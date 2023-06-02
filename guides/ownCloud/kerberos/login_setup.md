# How to set up Kerberos authentication for ownCloud

## Prerequisites
* Windows Server with Active Directory (Windows Server 2022)
* Windows Server with WND Service (Windows Server 2022)
* Windows Client (in our case another Windows Server 2022)
* ownCloud Server (Server with Ubuntu 20.04)

## Install and Configure Windows Active Directory
1. [Create a server at Hetzner Cloud using the Windows Server 2022 snapshot]
2. Setup Windows (Console on Hetzner webpage)
3. Update Windows
4. Set a new computer name
5. Disable IPV6
6. Change DNS Server
7. Add Role "Active Directory Domain Services"
8. Promote Server to Active Directory Domain Server
9. Add Users and Admins
10. Create Service User
    * New user "krb5httpoc" (for example) -> password never expired
    * Create keytab file for the account in windows cmd shell
    ```cmd
    ktpass /princ HTTP/ocserver.oc.com@OCSERVER.OC.COM /mapuser krb5httpoc +rndPass /out ocserver.oc.com.keytab /crypto all /ptype KRB5_NT_PRINCIPAL /mapop set
    ```




## Install and Configure owncloud Server
1. Create a server at Hetzner Cloud with ubuntu20.04 as chosen OS
2. Update Ubuntu
3. Install ownCloud Server
4. Enable LDAP app, connect to Active Directory, sync users from Active Directory



[Create a server at Hetzner Cloud using the Windows Server 2022 snapshot]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/server2022/create_hetzner_snapshot.md