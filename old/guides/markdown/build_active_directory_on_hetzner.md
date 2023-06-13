# How to build a Windows Active Directory with Servers on Hetzner hcloud

## Prerequisites
* 1 Server with Windows Server 2022 installed
* A FQDN which points to the Windows Server on Hetzner hcloud

## Create Server on Hetzner hcloud
1. Go to the Project where the Active Directory should be build

   

   :[owncloud kerberos setup][https://github.com/GeraldLeikam/tutorials/blob/master/guides/owncloud_kerberos_setup.md]

    <details>
      <summary>How do I dropdown?</summary>
      <br>

      test

    </details>

   ![image](/old/imagesages/hetzner_hcloud_project_overview.png)

2. Click "Add Server"

    ![image](/old/imagesages/hetzner_hcloud_project_overview_add_server_button.png)

3. Select Server Location (recommended is 'Nuremberg')

   ![image](/old/imagesages/hetzner_create_windows_server_2022_active_directory_location.png)

4. Select the image for Windows Server 2022 (By default Hetzner has no image for Windows Server 2022. But we created a Snapshot with a pre-installed Windows Server 2022 installation.) Click on Snapshots

   ![image](/old/imagesages/hetzner_create_windows_server_2022_active_directory_image.png)

5. Select the Snapshot 'winServer2022-sysprep' (If you don't have these Snapshot in your Project, please contact us. Then we build a Server for you which one of our Administrators can move to your Project)

   ![images](/old/imagesages/hetzner_create_windows_server_2022_active_directory_snapshots.png)

6. Select th Server Type (recommended is CX41)

   ![image](/old/imagesages/hetzner_create_windows_server_2022_active_directory_server_type.png)

7. Make sure that Public IPv4 and IPv6 is selected and select Private networks

   ![image](/old/imagesages/hetzner_create_windows_server_2022_active_directory_networking.png)

8. Select a private network for the Windows Active Directory. (The private network is for the actual communication of the servers that belong to the Windows Active Directory. If no private network is chosen, the communication of the servers must take place over the internet, which means that all communication must be encrypted. Also, for unencrypted communication, ports are opened on the server, which could result in an abuse message from the [BSI](https://www.bsi.bund.de). Therefore, a private network that is isolated from the public internet should always be used for Active Directory communication.)

   ![image](/old/imagesages/hetzner_create_windows_server_2022_active_directory_networking_private_network.png)