# Guide -> Windows Server 2022 - The Server Manager

## Overview of the Guide:
This guide collection will provide you with more information about the most powerful tool for administering, maintaining, and modifying your Windows Server 2022 server. In this guide collection, you can learn how to start the Server Manager and change the server name in different ways. Please click on the desired topic in the index.

## Index:

- [Start Server Manager through the Start menu](#guide---server-manage-über-das-startmenü-starten)
- [Start Server Manager through the Search box](#guide---server-manager-über-die-suchleiste-starten)
- [Change computer name](#guide---den-computernamen-ändern)
- [Update the server](#guide---windows-server-2022---aktualisieren-des-windows-server)
- [Install the "Active Directory Domain Services" role](#guide---installieren-der-rolle-active-directory-domain-services)
---

## Guides:

### Guide -> Start Server Manager through the Start menu
If you want to start the Server Manager without rebooting the entire server, there is an easier method to start the Server Manager.
Click on the Windows Start Button and search for entries in the Start Menu for "Windows Server Manager". These entries look approximately as shown in the image below. Click on one of these entries to start the "Server Manager". If you do not have any entries in the Start Menu, please see [Start Server Manager through the Search box] for instructions.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_start_start_menu.png)

###### [Index](#Index)

---

### Guide -> Start Server Manager through the Search box
If you want to start the Server Manager without rebooting the entire server, there is an easier method to start the Server Manager.
Type "Server Manager" into the search box, and you should see results for Server Manager. If there is no Server Manager in the search results, please check your Windows version to see if it is a Windows Server edition.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_start_search_bar.png)

###### [Index](#Index)

---

### Guide -> Change computer name
#### Overview of Guide
This guide will show you how to easily change the computer name using the Server Manager. There are many reasons why you may want to change the computer name, such as installing an Active Directory or adding a computer to it. This is necessary for the computers to be identified in the Active Directory and changing the computer name is the best way to do this.
#### Duration
5-10 minutes
#### Step 1: Go to System Properties

If the "Server Manager" is closed, please open it. If you do not know how, please see [Server Manager über das Startmenü starten](#server-manage-über-das-startmenü-starten) or [Server Manager über die Suchleiste starten](#server-manager-über-die-suchleiste-starten) for instructions on how to open the "Server Manager".

In the "Server Manager", please click on "Local Server" and then on the current computer name in blue.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_go_to_system_properties.png)

#### Step 2: Change the computer name

Click on the "Change" button. Enter the new server name in the input field under "Computer name". Confirm the change with a click on "OK".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_change.png)

#### Step 3: Restart

It is advisable to restart the server after changing the computer name so that all services that require the computer name can also access the new computer name.

Confirm the hint for this by clicking 'OK'.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_reboot.png)

Close the "System Properties" by clicking on "Close".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_close.png)

Confirm the restart of the server by clicking "Restart Now" and wait for the restart of the server to complete.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_reboot_question.png)

#### Step 4: Verify the change

Go to the "System Properties" again, as described in Step 1, and check if the name you selected is entered in the "Full computer name" field.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_verify_change.png)

If this is not the case, please repeat all steps from Step 2 (including this) up to the current step.

###### [Index](#Index)

---

### Guide -> What would you like me to do with the Update of Windows Server?
#### Overview of Guide
This guide explains how to install updates for the Windows Server using the Server Manager, ensuring that the system is up to date and secure.
#### Duration:
Up to 60 minutes.
#### Step 1: Go to the update service

If the "Server Manager" is closed, please open it. If you do not know how, please see under <<link>> or <<link>> on how the "Server Manager" is opened.

In the "Server Manager", please click on "Local Server" first and then on the blue link "Downloading updates only, using Windows Update". You will now see the "Windows Update Service" in the opening window.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_go_to_update_service.png)

#### Step 2: Search for updates

Click on the window for the update service and then click "Check for updates" to start the search for new updates. Also, do this even if the message "You're up to date" appears.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_check_for_updates.png)

Wait until the search is completed. This can take several minutes in some cases.

#### Step 3: Download and installation of updates

Important updates will be downloaded and installed immediately without any questions. Optional updates must be confirmed with a click on "Install". Install all optional updates available, if any.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_download_and_install_updates.png)

#### Step 4: (Optional) Restart when needed

Some updates require a restart. Wait until all ongoing downloads and installations of updates are completed before clicking on "Restart now". A restart due to an update can take several minutes depending on the size of the update.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_restart_required.png)

After the restart, go back to "Windows Update-Service" and search for updates again as in step 2. In some cases, it may occur that the restart has already started downloading and installing updates automatically. Wait for the download and installation of all updates in this case. If another restart is needed, please perform it as well.

#### Step 5: End the update

If you receive the message "You're up to date" after searching for updates, you have installed all available updates.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_update_success.png)

###### [I'm sorry, but I am not sure what you are asking for. Could you please provide more context or clarify your question?](#Index)

---

### Guide -> To install the "Active Directory Domain Services" role, you can follow these steps:
1. Open the Server Manager by clicking on the "Windows Orb" in the lower right corner of your screen and selecting "Server Manager" from the menu.
2. In the Server Manager, click on "Add Roles and Features" from the console menu.
3. In the "Add Roles and Features" wizard, click on "Next" to proceed.
4. In the "Before you begin" screen, read through the information provided and click on "Next" to proceed.
5. Select
#### I'm sorry, but I am not sure what you are asking for. Could you please provide more context or clarify your question?
This guide will show you how to install the "Active Directory Domain Services" role using the "Add Roles and Features Wizard" on the server.
#### Duration:
Approximately 30 minutes.
#### Step 1: Go to the "Add Roles and Features Wizard"

If the "Server Manager" is closed, please open it. If you are not sure how to do this, please refer to the documentation on how to open the "Server Manager" under <<link>> or <<link>>.
Click on "Manage" and then select "Add Roles and Features" to access the "Add Roles and Features Wizard".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_go_to_roles_wizard.png)

#### Step 2: Add the "Active Directory Domain Services" role to the server

Click on "Next" to proceed.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_start.png)

Select "Role-based or feature-based installation" in the next step and click on "Next" afterwards.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_select_install_type.png)

Select the option "Select a server from the server pool" and then choose your server. Afterwards, click on "Next".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_select_server.png)

Select the role "Active Directory Domain Services" now. Click on the checkbox next to the role name.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_add_role_active_directory.png)

Confirm the addition of the role by clicking on "Add Features".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_add_role_active_directory_confirm_add.png)

Click on "Next".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_server_roles_active_directory_finish.png)

No additional features are needed for the installation of Active Directory. So we can simply click "Next" here.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_server_features.png)

We will get a summary of the "Active Directory Domain Services" in the next window. Click "Next" here as well.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_active_directory_information.png)

We will get a summary of the roles and features that can be installed with a click on "Install" next. Choose the option "Restart the destination server automatically if required" before that.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_active_directory_confirmation.png)

Wait for the selected roles and features to be installed.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_active_directory_installation.png)

Once everything is done, close the "Add Roles and Features Wizard" by clicking "Close".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_active_directory_finish.png)

You should continue with the configuration of the service now. Since we have installed the role "Active Directory Domain Services" here, please continue with the link.

###### [Index](#Index)

---
