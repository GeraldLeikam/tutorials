# Guide -> install kerberos login on a ownCloud Server
## Prerequisites
- [A server with an installed ownCloud server software and SSL certificate]
- A server with WindowsServer2022 on which Active Directory is installed and configured
- A Windows client (for testing -> Note: Kerberos login only works with a Windows client)
- A private network in which all 3 servers are located (preferably at Hetzner)

## Step1: Copy Keytab file to ownCloud Server
Kopiere die Keytab file von deinem Rechner auf den ownCloud Server. Hierzu gibt es mehrere wege. 

Zum kopieren haben wir folgende Möglichkeiten:
- #### [Using the installed ```ownCloud```]
- #### [Using ```scp```]
- #### über sftp mit fileZilla

## Step1: Install recommended packages for kerberos
Downloade und Installiere die folgenden für kerberos benötigten Packete
```bash
apt install -y libkrb5-dev krb5-user msktutil
```
## Step2: Add kerberos host to hosts file
Setze den Eintrag in die hosts Datei mit folgendem Kommando. Ersetze vorher <<KERBEROS_HOST_IP>> und <<KERBEROS_HOST_DOMAIN>> durch deine eingene daten.
```bash
sed -i "11i<<KERBEROS_HOST_IP>> <<KERBEROS_HOST_DOMAIN>>\n" /etc/hosts
```
Deine hosts datei sollte danach in etwa so aussen:
```bash
root@oc01:/# cat /etc/hosts
# Your system has configured 'manage_etc_hosts' as True.
# As a result, if you wish for changes to this file to persist
# then you will need to either
# a.) make changes to the master file in /etc/cloud/templates/hosts.debian.tmpl
# b.) change or remove the value of 'manage_etc_hosts' in
#     /etc/cloud/cloud.cfg or cloud-config from user-data
#
127.0.1.1 oc01.kerberos.test.owncloud.works oc01
127.0.0.1 localhost

10.11.0.2 ad01.kerberos.test.owncloud.works

# The following lines are desirable for IPv6 capable hosts
::1 localhost ip6-localhost ip6-loopback
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters
```
## Step3: Create krb5 conf file
Um die konfigurationsdatei für krb5 zu erstellen nutze folgendes kommando nachdem du deine daten eingraten hast.
```bash
/bin/cat <<EOM >"/etc/krb5.conf"
[libdefaults]
        default_realm = <<your.domain.name>>
        rdns = no
        dns_lookup_kdc = false
        dns_lookup_realm = false

# The following krb5.conf variables are only for MIT Kerberos.
        kdc_timesync = 1
        ccache_type = 4
        forwardable = true
        proxiable = true

# The following encryption type specification will be used by MIT Kerberos
# if uncommented.  In general, the defaults in the MIT Kerberos code are
# correct and overriding these specifications only serves to disable new
# encryption types as they are added, creating interoperability problems.
#
# The only time when you might need to uncomment these lines and change
# the enctypes is if you have local software that will break on ticket
# caches containing ticket encryption types it doesn't know about (such as
# old versions of Sun Java).

#       default_tgs_enctypes = des3-hmac-sha1
#       default_tkt_enctypes = des3-hmac-sha1
#       permitted_enctypes = des3-hmac-sha1

# The following libdefaults parameters are only for Heimdal Kerberos.
        fcc-mit-ticketflags = true

[realms]
        <<your.domain.name>> = {
                kdc = <<your.Active.Directory.Server>>
                admin_server = <<your.Active.Directory.Server>>
        }
[domain_realm]
        .<<your.domain.name>> = <<your.domain.name>>
EOM
}
```

## Step1: Install and enable kerberos_app
Download the [latest release of the Kerberos app] from GitHub to your computer.

Copy the kerberos-X.X.X.tar.gz file to your server (it is recommended to [use scp] for this).

Log in via ssh to your server and navigate to the kerberos-X.X.X.tar.gz file. 

Unpack the file and move the "app" folder to "/var/www/owncloud/apps-external". 

Activate the app using the command: 
```base
"occ app:enable appname"
```

[A server with an installed ownCloud server software and SSL certificate]: https://github.com/GeraldLeikam/tutorials/blob/master/ownCloud/install_owncloud_full.md
[latest release of the Kerberos app]: https://github.com/owncloud/kerberos/tags
[use scp]: https://github.com/GeraldLeikam/tutorials/blob/master/linux/scp-copy_to_remote.md
[Using ```scp```]: https://github.com/GeraldLeikam/tutorials/blob/master/linux/scp-copy_to_remote0.md
[Using the installed ```ownCloud```]: https://github.com/GeraldLeikam/tutorials/blob/master/ownCloud/upload_a_file_via_webinterface_and_use_it_in_ssh_session.md