# Guide -> Windows Server 2022 - The Server Manager

## Overview of the Guide:
This guide collection will provide you with more information about the most powerful tool for administering, maintaining, and modifying your Windows Server 2022 server. In this guide collection, you can learn how to start the Server Manager and change the server name in different ways. Please click on the desired topic in the index.

## Index:

- [Start Server Manager through the Start menu](#guide---server-manage-über-das-startmenü-starten)
- [Start Server Manager through the Search box](#guide---server-manager-über-die-suchleiste-starten)
- [Change computer name](#guide---den-computernamen-ändern)
- [Update the server](#guide---windows-server-2022---aktualisieren-des-windows-server)
---

## Guides:

### Guide -> Start Server Manager through the Start menu
If you have already shot the Server Manager and still need it, there is an easier way to start the Server Manager without rebooting the entire server.
Click on the Windows Start Button and search for entries in the Start Menu for Windows Server Manager. These look approximately as shown in the image below. Click on one of these entries to start the "Server Manager". If you do not have any in the Start Menu, please see [Start Server Manager through the Search box] below.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_start_start_menu.png)

###### [Index](#Index)

---

### Guide -> Start Server Manager through the Search box
If you have already shot the Server Manager and still need it, there is an easier way to start the Server Manager without rebooting the entire server.
Type "Server Manager" into the search box and if it appears in the search results, click on it to start the Server Manager. If there is no Server Manager in the search results, please check your Windows version to see if it is a Windows Server edition.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_start_search_bar.png)

###### [Index](#Index)

---

### Guide -> Change computer name
#### Guide Overview:
Changing the computer name can have various reasons. For example, you may want to install an Active Directory or add a computer to it, which is essential for identifying the computers in the Active Directory and this is best done with a self-explanatory name. This guide will show you how easy it is to change the computer name using the Server Manager.
#### Duration:
5-10 minutes
#### Step 1: Go to System Properties

If the "Server Manager" is closed, please open it. If you do not know how, please see [Server Manager über das Startmenü starten](#server-manage-über-das-startmenü-starten) or [Server Manager über die Suchleiste starten](#server-manager-über-die-suchleiste-starten) to find out how the "Server Manager" is opened.

In the "Server Manager", please click on "Local Server" and then on the current computer name.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_go_to_system_properties.png)

#### Step 2: Change the computer name

Click on the "Change" button. Enter the new computer name in the input field under "Computer name". Confirm the change with a click on "OK".

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

### Guide -> Windows Server 2022 - Updating Windows Server
#### Guide Overview
This guide explains how to install updates for the Windows Server using the Server Manager, ensuring that the system is up-to-date and secure.
#### Duration
Up to 60 minutes.
#### Step 1: Go to the update service

If the "Server Manager" is closed, please open it. If you do not know how, please see [Server Manager über das Startmenü starten](#server-manage-über-das-startmenü-starten) or [Server Manager über die Suchleiste starten](#server-manager-über-die-suchleiste-starten) to find out how the "Server Manager" is opened.

In the "Server Manager", please click on "Local Server" first and then on the blue link "Downloading updates only, using Windows Update". You will now see the "Windows Update Service" in the opening window.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_go_to_update_service.png)

#### Step 2: Search for updates

Click on the window for the update service and then click "Check for updates" to start searching for new updates. Also, do this even if the message "You're up to date" appears.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_check_for_updates.png)

Wait until the search is completed. This can take several minutes in some cases.

#### Step 3: Download and installation of updates

Important updates will be downloaded and installed without any questions. Optional updates must be confirmed with a click on "Install". Install all optional updates available, if any.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_download_and_install_updates.png)

#### Step 4: (Optional) Restart when necessary

Some updates require a restart. Wait until all downloads and installations of updates are completed before clicking on "Restart now". A restart due to an update can take several minutes, depending on the size of the update.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_restart_required.png)

After the restart, go back to the "Windows Update Service" as you did in Step 1 and search for additional updates as you did in Step 2. In some cases, it may occur that the restart has already started downloading and installing updates automatically. Wait for the download and installation of all updates in this case. If another restart is required, please perform it as well.

#### Step 5: End the update

If you receive the message "You're up to date" after searching for updates, you have installed all available updates.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_update_success.png)

###### [Index](#Index)

---
