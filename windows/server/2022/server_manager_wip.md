# Guide -> Windows Server 2022 - The Server Manager

## Overview of the Guide:
This guide collection will provide you with more information about the most powerful tool for administering, maintaining, and modifying your Windows Server 2022 server. In this guide collection, you can learn how to start the Server Manager and change the server name in different ways. Please click on the desired topic in the index.

## Index:

- [Start Server Manager through the Start menu](#guide---start-server-manager-through-the-start-menu)
- [Start Server Manager through the Search box](#guide---start-server-manager-through-the-search-box)
- [Change the computer name](#guide---change-the-computer-name)
- [Updaten des Servers](#guide---windows-server-2022---the-server-manager)
---

## Guides:

### Guide -> Start Server Manager through the Start menu
If you have already shot the Server Manager and still need it, there is an easier way to start the Server Manager without rebooting the entire server.
Click on the Windows Start Button and search for entries in the Start Menu for Windows Server Manager. These look approximately as shown in the image below to see. Click one of these entries to start the "Server Manager". If you do not have any in the Start Menu, please see [Start Server Manager through the Search box] for instructions.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_start_start_menu.png)

###### [Index](#Index)

---

### Guide -> Start Server Manager through the Search box
If you have already shot the Server Manager and still need it, there is an easier way to start the Server Manager without rebooting the entire server.
Type "Server Manager" into the search box and if it appears in the search results, click on it to start the Server Manager. If there is no Server Manager in the search results, please check your Windows version to see if it is a Windows Server edition.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_start_search_bar.png)

###### [Index](#Index)

---

### Guide -> Change the computer name
#### Overview of Guide
This guide will show you how to easily change the computer name using the Server Manager. There are many reasons why you may want to do this, such as installing an Active Directory or adding a computer to it. In order for the computers to be identified correctly in the Active Directory, it is necessary to give them unique names, which can be easily done with the Server Manager.
#### Duration
5-10 minutes
#### Step 1: Go to System Properties

If the "Server Manager" is closed, please open it. If you do not know how, please see [Start Server Manager through the Start menu](#guide---start-server-manager-through-the-start-menu) or [Start Server Manager through the Search box](#guide---start-server-manager-through-the-search-box) for instructions on how to open the "Server Manager".

In the "Server Manager", please click on "Local Server" and then on the current computer name.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_go_to_system_properties.png)

#### Step 2: Change the computer name

Click on the "Change" button. Enter the new server name in the text field under "Computer name". Confirm the change with a click on "OK".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_change.png)

#### Step 3: Restart

It is advisable to restart the server after changing its name so that all services that require the computer name can also access the new computer name.

Confirm the hint for this by clicking "OK".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_reboot.png)

Close the "System Properties" by clicking on "Close".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_close.png)

Confirm the restart of the server by clicking "Restart Now" and wait for the restart of the server.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_reboot_question.png)

#### Step 4: Verify the change

Go to the "System Properties" again, as described in step 1, and check if the name you selected is entered in the "Full computer name" field.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_verify_change.png)

If this is not the case, please repeat all steps from step 2 (including this) again.

###### [Index](#Index)
