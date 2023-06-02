# How to set up Kerberos authentication for ownCloud

## Prerequisites
* Windows Server with Active Directory (Windows Server 2022)
* Windows Server with WND Service (Windows Server 2022)
* Windows Client (in our case another Windows Server 2022)
* ownCloud Server (Server with Ubuntu 20.04)

## Install and Configure Windows Active Directory
1. [Create a server at Hetzner Cloud using the Windows Server 2022 snapshot]
2. [Setup Windows (Console on Hetzner webpage)]
3. [Setup RDP connection via Remmina (optional)]
4. [Update Windows]
5. [Change computer name]
6. [Disable IPV6 connectivity]
7. [Change DNS Server]
8. [Add Role "Active Directory Domain Services"]
9. [Promote Server to Active Directory Authority]
10. [Create Users, Groups and Admins]
11. Add the created users to the created groups
12. Create Service User
    




## Install and Configure owncloud Server
1. Create a server at Hetzner Cloud with ubuntu20.04 as chosen OS
2. Update Ubuntu
3. Install ownCloud Server
4. Enable LDAP app, connect to Active Directory, sync users from Active Directory



[Create a server at Hetzner Cloud using the Windows Server 2022 snapshot]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/server2022/create_hetzner_snapshot.md
[Setup Windows (Console on Hetzner webpage)]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/server2022/finish_setup_hetzner_webconsole.md
[Setup RDP connection via Remmina (optional)]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/server2022/setup_rdp_remmina.md
[Update Windows]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/server2022/update_windows.md
[Change computer name]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/change_computer_name.md
[Disable IPV6 connectivity]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/disable_ipv6_connectivity.md
[Change DNS Server]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/change_dns_server.md
[Add Role "Active Directory Domain Services"]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/install_active_directory_role.md
[Promote Server to Active Directory Authority]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/promote_server_to_active_directory.md
[Create Users, Groups and Admins]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/windows/create_users_groups_admins.md