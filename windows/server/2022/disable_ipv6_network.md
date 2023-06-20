# Guide -> Windows Server 2022 - Disable IPV6 Network Connection(s).
## Guide Overview.
In this guide, instructions will be provided on how to disable IPV6 network connection(s) on a Windows Server 2022.
## Needed Time: [insert specific time or duration of task].
About 5 minutes.
## Step1: Go to Server Manager.
Go to Server Manager and select on the left side "Local Server".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6.png)

## Step2: Go to Network Connections.
If you have multiple interfaces, click on any one. The interface you choose does not matter. If you only have one interface, click on it.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_select_interface.png)

## Step3: Open Interface and disable IPV6.
Select the interface you want to disable IPV6 and click twice on it.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_network_connections.png)

After that, click on "Properties".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_network_connection_properties.png)

Now select the option "Internet Protocol Version 6 (TCP/IPv6)".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_select_option.png)

And disable the option by unchecking the checkbox. Then please click on "OK".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_deselect_option.png)

Close the interface by clicking on "Close".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_close_interface.png)

Repeat the previous steps for all interfaces where you want to disable IPV6 connectivity.
After that, close the "Network Connections" window and click on the "Server Manager" to refresh "Local Server".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_refreh_server_manager.png)

Your network connection/s in the "Server Manager" under "Local Server" should now appear approximately as shown here.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_deactivated.png)
