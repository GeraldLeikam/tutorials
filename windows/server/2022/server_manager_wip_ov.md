# Guide -> Windows Server 2022 - Der Server Manager

## Guide Overview:
Dieser Guide soll dir mehr Informationen über das wohl leistungsstärkste Tools zur Verwaltung, Wartung und Modifikation deines Windows Server 2022 Servers geben. In dieser Guide-Sammlung kannst du erfahren wie du den Server Manager auf unterschiedliche weise startest und den Namen des Servers änderst. Klicke bitte hierfür im Index auf das gewünschte Thema.    

## Index:

* [Server Manager über das Startmenü starten](#guide---server-manage-über-das-startmenü-starten)
* [Server Manager über die Suchleiste starten](#guide---server-manager-über-die-suchleiste-starten)
* [Den Computernamen ändern](#guide---den-computernamen-ändern)

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