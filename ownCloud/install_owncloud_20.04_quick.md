# Guide -> install ownCloud on a server with Ubuntu 20.04
## Prerequisites
 - A server with Ubuntu20.04(preferably Hetzner Cloud)
 - SSH root access on this server
## Step 1: Preparation
### Set your Domain Name
```bash
my_domain="Your.Domain.tld"
echo $my_domain

hostnamectl set-hostname $my_domain
hostname -f
```
### Generate Strong Passwords
```bash
sec_admin_pwd=$(openssl rand -base64 18)
echo $sec_admin_pwd > /etc/.sec_admin_pwd.txt

sec_db_pwd=$(openssl rand -base64 18)
echo $sec_db_pwd > /etc/.sec_db_pwd.txt
```
### Update Your System
Initially, you need to update your Ubuntu system to the latest packages:
```bash
sudo apt update
sudo apt upgrade -y
```
### Create the occ Helper Script
Create a helper script to simplify running occ commands:
```bash
FILE="/usr/local/bin/occ"
cat <<EOM >$FILE
#! /bin/bash
cd /var/www/owncloud
sudo -E -u www-data /usr/bin/php /var/www/owncloud/occ "\$@"
EOM
```
Make the helper script executable:
```bash
chmod +x $FILE
```
### Install the Required Packages
```bash
apt install -y \
apache2 libapache2-mod-php \
mariadb-server openssl redis-server wget php-imagick \
php-common php-curl php-gd php-gmp php-bcmath php-imap \
php-intl php-json php-mbstring php-mysql php-ssh2 php-xml \
php-zip php-apcu php-redis php-ldap php-phpseclib
```
### Install smbclient php Module
If you want to connect to external storage via SMB you need to install the smbclient php module.
First install the required packages:
```bash
apt-get install -y libsmbclient-dev php-dev php-pear
```
Then install smblclient php module using pecl:
```bash
pecl channel-update pecl.php.net
mkdir -p /tmp/pear/cache
pecl install smbclient-stable
echo "extension=smbclient.so" > /etc/php/7.4/mods-available/smbclient.ini
phpenmod smbclient
systemctl restart apache2
```
Check if it was successfully activated:
```bash
php -m | grep smbclient
```
This should show the following output:
```bash
libsmbclient
smbclient
```
### Install the Recommended Packages
Additional useful tools helpful for debugging:
```bash
apt install -y \
unzip bzip2 rsync curl jq \
inetutils-ping  ldap-utils \
smbclient
```
### Configure Apache
#### Create a Virtual Host Configuration
```bash
FILE="/etc/apache2/sites-available/owncloud.conf"
cat <<EOM >$FILE
<VirtualHost *:80>
ServerName $my_domain
DirectoryIndex index.php index.html
DocumentRoot /var/www/owncloud
<Directory /var/www/owncloud>
Options +FollowSymlinks -Indexes
AllowOverride All
Require all granted

 <IfModule mod_dav.c>
  Dav off
 </IfModule>

SetEnv HOME /var/www/owncloud
SetEnv HTTP_HOME /var/www/owncloud
</Directory>
</VirtualHost>
EOM
```
#### Enable the Virtual Host Configuration
```bash
a2dissite 000-default
a2ensite owncloud.conf
```
### Configure the Database
It’s recommended to execute mysql_secure_installation to secure the mariadb installation and set a strong password for the database user.
Ensure transaction-isolation level is set and performance_schema on.
```bash
sed -i "/\[mysqld\]/atransaction-isolation = READ-COMMITTED\nperformance_schema = on" /etc/mysql/mariadb.conf.d/50-server.cnf
systemctl start mariadb
mysql -u root -e "CREATE DATABASE IF NOT EXISTS owncloud; \
GRANT ALL PRIVILEGES ON owncloud.* \
TO owncloud@localhost \
IDENTIFIED BY '${sec_db_pwd}'";
```
It is recommended to run mysqltuner script to analyse database configuration after running with load for several days.
#### Enable the Recommended Apache Modules
```bash
a2enmod dir env headers mime rewrite setenvif
systemctl restart apache2
```
## Step 2: Installation
### Download ownCloud
```bash
cd /var/www/
wget https://download.owncloud.com/server/stable/owncloud-complete-latest.tar.bz2 && \
tar -xjf owncloud-complete-latest.tar.bz2 && \
chown -R www-data. owncloud
```
### Install ownCloud
Remember to set a strong password for your owncloud admin user and provide the previously set password for the database user as the --database-pass argument.
```bash
occ maintenance:install \
--database "mysql" \
--database-name "owncloud" \
--database-user "owncloud" \
--database-pass ${sec_db_pwd} \
--data-dir "/var/www/owncloud/data" \
--admin-user "admin" \
--admin-pass ${sec_admin_pwd}
```
### Configure ownCloud’s Trusted Domains
```bash
my_ip=$(hostname -I|cut -f1 -d ' ')
occ config:system:set trusted_domains 1 --value="$my_ip"
occ config:system:set trusted_domains 2 --value="$my_domain"
```
### Configure the cron Jobs
Set your background job mode to cron:
```bash
occ background:cron
```
Configure the execution of the cron job to every 15 min and the cleanup of chunks every night at 2 am:
```bash
echo "*/15  *  *  *  * /var/www/owncloud/occ system:cron" \
| sudo -u www-data -g crontab tee -a \
/var/spool/cron/crontabs/www-data
echo "0  2  *  *  * /var/www/owncloud/occ dav:cleanup-chunks" \
| sudo -u www-data -g crontab tee -a \
/var/spool/cron/crontabs/www-data
```
If you need to sync your users from an LDAP or Active Directory Server, add this additional Cron job. Every 4 hours this cron job will sync LDAP users in ownCloud and disable the ones who are not available for ownCloud. Additionally, you get a log file in /var/log/ldap-sync/user-sync.log for debugging.
```bash
echo "1 */6 * * * /var/www/owncloud/occ user:sync \
'OCA\User_LDAP\User_Proxy' -m disable -vvv >> \
/var/log/ldap-sync/user-sync.log 2>&1" \
| sudo -u www-data -g crontab tee -a \
/var/spool/cron/crontabs/www-data
mkdir -p /var/log/ldap-sync
touch /var/log/ldap-sync/user-sync.log
chown www-data. /var/log/ldap-sync/user-sync.log
```
### Configure Caching and File Locking
```bash
occ config:system:set \
memcache.local \
--value '\OC\Memcache\APCu'
occ config:system:set \
memcache.locking \
--value '\OC\Memcache\Redis'
occ config:system:set \
redis \
--value '{"host": "127.0.0.1", "port": "6379"}' \
--type json
```
### Configure Log Rotation
```bash
FILE="/etc/logrotate.d/owncloud"
sudo cat <<EOM >$FILE
/var/www/owncloud/data/owncloud.log {
size 10M
rotate 12
copytruncate
missingok
compress
compresscmd /bin/gzip
}
EOM
```
### Finalize the Installation
Make sure the permissions are correct:
```bash
cd /var/www/
chown -R www-data. owncloud
```

To check if you have installed the correct version of ownCloud and that the occ command is working, execute the following:
```bash
occ -V
echo "Your Admin password is: "$sec_admin_pwd
echo "It's documented at /etc/.sec_admin_pwd.txt"
echo "Your Database Password is: "$sec_db_pwd
echo "It's documented at /etc/.sec_db_pwd.txt and in your config.php"
echo "Your ownCloud is accessable under: "$my_domain
echo "The Installation is complete."
```