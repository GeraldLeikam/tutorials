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

[create a private network]: https://github.com/GeraldLeikam/tutorials/blob/master/guides/hetzner/create_a_private_network.md