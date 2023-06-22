# Guide -> Windows Server 2022 - Der Server Manager

## Guide Overview:
Dieser Guide-Sammlung soll dir mehr Informationen über das wohl leistungsstärkste Tools zur Verwaltung, Wartung und Modifikation deines Windows Server 2022 Servers geben. In dieser Guide-Sammlung kannst du erfahren wie du den Server Manager auf unterschiedliche weise startest und den Namen des Servers änderst. Klicke bitte hierfür im Index auf das gewünschte Thema.    

## Index:

* [Server Manager über das Startmenü starten](#guide---server-manage-über-das-startmenü-starten)
* [Server Manager über die Suchleiste starten](#guide---server-manager-über-die-suchleiste-starten)
* [Den Computernamen ändern](#guide---den-computernamen-ändern)
* [Den Server aktualisieren](#guide---windows-server-2022---aktualisieren-des-windows-server)
---

## Guides

### Guide -> Server Manage über das Startmenü starten
Solltest du den Server Manager einmal geschossen und diesen jedoch doch benötigen gibt es eine einfachere Methode den Server Manager zu starten, ohne gleich den ganzen Server zu rebooten.
Klicke auf den Windows Start Button und suche im Start Menu nach den Einträgen für den Windows Server Manager. Diese sehen ungefähr so wie im Bild weiter unten zu sehen ist aus. Klicke einen dieser Einträge um den "Server Manager zu starten". Solltest du keine im Start Menu haben so siehe bitte unter [Server Manager über die Suchleiste starten] nach.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_start_start_menu.png)

###### [Index](#Index)

---

### Guide -> Server Manager über die Suchleiste starten
Solltest du den Server Manager einmal geschossen und diesen jedoch doch benötigen gibt es eine einfachere Methode den Server Manager zu starten, ohne gleich den ganzen Server zu rebooten.
Klicke in die Suchleiste und gib "Server Manager" ein darauf hin sollte in den Suchergebnissen der Server Manager enthalten sein. Sollte hier kein Server Manager enthalten sein so prüfe bitte die Version deines Windows, ob es sich hierbei um eine Windows Server Version handelt.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_start_search_bar.png)

###### [Index](#Index)

---

### Guide -> Den Computernamen ändern
#### Guide Overview:
Das Ändern des Computernamens kann viele Gründe haben. Möchtest du z.B. ein Active Directory installieren oder einen Rechner einem hinzufügen, ist dies unbedingt notwendig und die Rechner in dem Active Directory irgendwie identifiziert werden müssen und dies am besten mit einem für sich selbst sprechenden Namen geht. Dieser Guide soll zeigen wie einfach es ist mit dem Server Manager den Namen des Servers zu ändern.
#### Dauer:
5-10 Minuten
#### Schritt 1: Gehe zu den System Properties

Sollte des "Server Manager" geschlossen sein so öffne diesen bitte. Solltest du nicht wissen wie, siehe bitte unter [Server Manager über das Startmenü starten](#server-manage-über-das-startmenü-starten) oder [Server Manager über die Suchleiste starten](#server-manager-über-die-suchleiste-starten) nach wie der "Server Manager" geöffnet wird.

Im "Server Manager" klicke bitte auf "Local Server" und anschließend auf den blauen aktuellen Computernamen.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_go_to_system_properties.png)

#### Schritt 2: Ändern des Computernamen

Klicke auf den "Change" Button. Trage in das Eingabefeld unter "Computer name" den neuen Namen des Servers ein. Bestätige die Änderung des Names mit einem Klick auf "OK".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_change.png)

#### Step 3: Neustart

Nach der Änderung des Computer Names is es sinnvoll den Server neu zu starten damit alle Dienste die den Computer Namen benötigen auch den neuen Computer Namen zur Verfügung haben. 

Bestätige den Hinweis hierfür mit 'OK'

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_reboot.png)

Schließe die "System Properties" durch einen Klick auf "Close" 

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_close.png)

Bestätige den Neustart des Servers mit einem Klick auf "Restart Now" und warte den Neustart des Servers ab.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_reboot_question.png)

#### Step 4: Verifiziere die Änderung

Gehe nach dem Server Neustart nochmals wie in Schritt 1 beschrieben zu den 'System Properties' und prüfe ob im Feld "Full computer name" der von dir gewählte name eingetragen ist. 

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/change_sever_name/windows_server_2022_change_servername_system_properties_verify_change.png)

Sollte dies nicht der Fall sein so wiederhole bitte ab Schritt 2 (inklusive diesem) alle weiteren Schritte.

###### [Index](#Index)

---

### Guide -> Windows Server 2022 - Aktualisieren des Windows Server
#### Guide Overview
Dieser Guide beschäftigt sich damit wie man mit dem Server Manager updates für den Windows Server installiert und dadurch das System aktuell und sicher hält.
#### Dauer:
up to 60 minutes.
#### Step1: Gehe zum update service

Sollte des "Server Manager" geschlossen sein so öffne diesen bitte. Solltest du nicht wissen wie, siehe bitte unter [Server Manager über das Startmenü starten](#server-manage-über-das-startmenü-starten) oder [Server Manager über die Suchleiste starten](#server-manager-über-die-suchleiste-starten) nach wie der "Server Manager" geöffnet wird.

Im "Server Manager" klicke bitte auf "Local Server" und anschließend auf den blauen Link "Downloading updates only, using Windows Update". Im sich darauf öffnenden siehst du nun den "Windows Update-Service".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_go_to_update_service.png)

#### Step2: Suche nach Updates

Klicke im Fenster für den Update-Service anschließend auf "Check for updates" um die Suche nach neuen Updates zu starten. Führe dies auch durch, auch wenn du die Meldung "You're up to date" erscheint.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_check_for_updates.png)

Warte bis die Suche abgeschlossen ist. Dies kann in manchen Fällen mehrere Minuten in Anspruch nehmen.

#### Step3: Download und Installation der Updates

Wichtige Updates werden sofort ohne Zwischenfragen heruntergeladen und installiert. Optionale Updates must du mit einem Klick auf "Install" bestätigen.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_download_and_install_updates.png)

#### Step4: (Optional) Neustart wenn benötigt

Manche Updates benötigen einen Neustart. Warte bist alle laufenden Downloads und Installation von Updates abgeschlossen sind bevor du auf "Restart now" klickst. Ein Restart wegen eines Updates kann mehrere Minuten dauern je nach größe des Updates.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_restart_required.png)

Nach dem Neustart gehe wieder wie in Schritt 1 zum "Windows Update-Service" und suche erneut wie in Schritt 2 nach weiteren Updates. Ich manchen Fällen kann es vorkommen das nach dem Neustart bereits weitere Updates automatisch angefangen haben zu downloaden und zu installieren. Warte in diesem Fall den Download und die Installation aller Updates ab. Sollte ein weiterer Neustart benötigt werden so führe auch diesen bitte aus. 

#### Step5: Beende das Update

Solltest du nach dem Suchen von Updates die Meldung "You're up to date" erhalten so hast du alle verfügbaren updates installiert.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_update_service_update_success.png)

###### [Index](#Index)

---
