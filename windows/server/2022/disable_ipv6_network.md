# Guide -> Disable IPV6 Connection(s) for Server
## Guide Overview
In diesem Guide wird erklärt wie bei einem Windows Server 2022 die IPV6 Verbindung(en) deaktiviert werden.
## Needed Time:
ca 5 Minuten
## Step1: Go to Server Manager
Gehe zum Server Manager und wähle auf linken Seite "Local Server"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6.png)

## Step2: Go to Network Connections
Klicke wenn du mehrere Interfaces hast auf irgend eines. Welches du wählst spielt keine Rolle. Solltest du nur ein Interface haben so klicke auf dieses.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_select_interface.png)

## Step3: Open Interface and disable IPV6
Wähle das Interface aus bei welchem du IPV6 deaktivieren willst und führe einen Doppelklick darauf aus. 

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_network_connections.png)

Klicke danach auf Properties

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_network_connection_properties.png)

Nun wähle die Option "Internet Protocol Version 6 (TCP/IPv6)"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_select_option.png)

und deaktiviere die Option durch abwählen des Kontrollkästchens. Anschließend klicke bitte auf "OK"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_deselect_option.png)

Schließe das Interface durch einen klick auf 'Close'

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_close_interface.png)

Wiederhole die bisherigen Schritte für alle Interfaces bei denen du die IPV6 Konnektivität deaktivieren möchtest.
Anschliessend schließe das "Network Connections" Fenster und klicke im "Server Manager" auf "Refesh 'Local Server'"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/disable_ipv6/windows_server_2022_disable_ipv6_refreh_server_manager.png)