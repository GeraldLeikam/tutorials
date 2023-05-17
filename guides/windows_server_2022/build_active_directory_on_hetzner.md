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

5. Select the Snapshot 'winServer2022-sysprep' (If you don't have these Snapshot in your Project, please contact us. Then we build a Server for you which one of our Administrators can move to your Project)

   ![images](/images/hetzner_create_windows_server_2022_active_directory_snapshots.png)

6. Select th Server Type (recommended is CX41)

   ![image](/images/hetzner_create_windows_server_2022_active_directory_server_type.png)

