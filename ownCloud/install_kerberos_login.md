# Guide -> install kerberos login on a ownCloud Server
## Prerequisites
- [A server with an installed ownCloud server software and SSL certificate]
- A server with WindowsServer2022 on which Active Directory is installed and configured
- A Windows client (for testing -> Note: Kerberos login only works with a Windows client)
- A private network in which all 3 servers are located (preferably at Hetzner)

## Step1: Install and enable kerberos_app
Download the [latest release of the Kerberos app] from GitHub to your computer.
Copy the kerberos-X.X.X.tar.gz file to your server (it is recommended to use scp for this).
Log in to your server and navigate to the app.tar.gz file. Unpack the file and move the "app" folder to "/var/www/owncloud/apps-external". Activate the app using the command "occ app:enable appname".


[A server with an installed ownCloud server software and SSL certificate]: https://github.com/GeraldLeikam/tutorials/blob/master/ownCloud/install_owncloud_full.md
[latest release of the Kerberos app]: https://github.com/owncloud/kerberos/tags