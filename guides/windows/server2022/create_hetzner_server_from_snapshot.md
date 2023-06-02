# Setup of a Windows Server 2022 Server at Hetzner Cloud using a snapshot

## Prerequisites
* coming soon

## Create Server
1. Login to Hetzner Cloud
2. Select your Project where the sever should build
3. Click "Add Server"
4. Choose your preferred location
5. In the images section, select the "Snapshots" tab.
6. Select the Snapshot: "winServer2022-sysprep"
7. Choose the server type of the server to be created (a server of the type CX31 is recommended)
8. Ensure that in the Network section, IPv4 and IPv6 are activated
9. Check the "Private networks" option and select the network to which the server should be added. If there is no private network for the server, create one. If you don't know how, refer to the guide [create a private network]. This will be used for communication of the servers in the Active Directory, as well as the owncloud with the Active Directory. Care should be taken that any communication of the Active Directory runs over an interface separate from the Internet.
10. Select at least one SSH key, even though Windows does not support SSH login. If no SSH key is selected, Hetzner will create a password for the server and send it by email. However, these emails are not received by you, but by our admin team, which is not very pleased with the recurring emails. Moreover, under Linux you would have no possibility to connect to the server via ssh as you don't have a password. If there is no SSH key in the project, add a valid SSH key. If you don't know how, please refer to the guide [add a ssh key to your Hetzner project].
11. If needed, select a volume for the server or add a new volume to the project
12. Please note that for a Windows Server, the volume should be added before the server is created, as adding it later can cause problems with the Windows Server. You can read how this works in the [add a volume while server creation to server] guide

[create a private network]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/hetzner/create_a_private_network.md
[add a ssh key to your Hetzner project]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/hetzner/add_ssh_key_to_project.md
[add a volume while server creation to server]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/hetzner/add_a_volume_while_server_creation_to_server.md