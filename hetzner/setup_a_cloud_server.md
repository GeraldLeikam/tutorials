# Guide -> Setup a Cloud Server at Hetzner Cloud

## Prerequisites
- a ssh key
- a [Hetzner Cloud Account]
## Step1: Setup Server
Select your project and click on "Add Server" on the right side in the server overview
### Location
Select the location of your server (recommended -> Nuremberg)
### Image
Select Ubuntu 20.04 as the image
### Type
The server type should be chosen according to the requirements. Normally, a server of the type CX21 is sufficient.
### Networking
Make sure that Public IPv4 and Public IPv6 are activated. Add the server to a private network if needed. Select or create a private network for this.
### SSH Keys
Select your SSH keys that should be entered on the server. At least one SSH key must always be selected!
### Volumes
Select or create a volume if you need more space. Note: Volumes are chargeable!
### Firewalls
Firewalls allow you to easily secure your servers by restricting or allowing traffic based on rules. Create or select a firewall. A firewall where only the ports that are needed are open is recommended.
### Backups
If you need backups of the server, activate this option. Note: This option is chargeable.
### Placement groups
If you need your servers to not all run on the same physical server but be distributed across different servers, add your servers to a placement group. (Alternatively, you can place all the servers you need for a project in a placement group to find them faster.)
### Labels
Labels are key-value pairs. Both key and value must be 63 characters or less, and must begin and end with an alphanumeric character. Alphanumerics or dashes, hyphens, and dots can be used in-between. Use the label {for} as a description for what the server is used for, and use the label {owner} with your name to indicate who owns this server. Alternatively, you can also add firewall rules based on labels.
### Cloud config
Ignore that. I also have no idea what it is for.
### Name
Give the server a meaningful name.
### Create & Buy now
Please double-check all the provided parameters once again. If everything looks correct, please click on "Create & Buy now."
### Finalize
Wait until your server is created. This should take no longer than a maximum of 3 minutes for a standard image like Ubuntu. If the image was a snapshot, creating the server may take several minutes.