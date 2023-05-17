# How to build a Windows Active Directory with Servers on Hetzner hcloud

## Prerequisites
* 1 Server with Windows Server 2022 installed
* A FQDN witch points to the Windows Server on Hetzner hcloud

## Create Server on Hetzner hcloud
1. Go to the Project where the Active Directory should be build

    ![image](/images/hetzner_hcloud_project_overview.png)

2. Click "Add Server"

    ![image](/images/hetzner_hcloud_project_overview_add_server_button.png)

3. Select Server Location (recommended is 'Nuremberg')

   ![image](/images/hetzner_create_windows_server_2022_active_directory_location.png)

4. Select the image for Windows Server 2022 (By default Hetzner has no image for Windows Server 2022. But we created a Snapshot with a pre-installed Windows Server 2022 installation.) Click on Snapshots

   ![image](/images/hetzner_create_windows_server_2022_active_directory_image.png)