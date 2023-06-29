# Guide -> Windows Server 2022 - Der Server Manager

## Guide Overview:
Dieser Guide-Sammlung soll dir mehr Informationen über das wohl leistungsstärkste Tools zur Verwaltung, Wartung und Modifikation deines Windows Server 2022 Servers geben. In dieser Guide-Sammlung kannst du erfahren wie du den Server Manager auf unterschiedliche weise startest und den Namen des Servers änderst. Klicke bitte hierfür im Index auf das gewünschte Thema.    

## Index:

* [Server Manager über das Startmenü starten](#guide---server-manage-über-das-startmenü-starten)
* [Server Manager über die Suchleiste starten](#guide---server-manager-über-die-suchleiste-starten)
* [Den Computernamen ändern](#guide---den-computernamen-ändern)
* [Den Server aktualisieren](#guide---windows-server-2022---aktualisieren-des-windows-server)
* [Die Rolle "Active Directory Domain Services" installieren](#guide---installieren-der-rolle-active-directory-domain-services)
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

### Guide -> Aktualisieren des Windows Server
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

Wichtige Updates werden sofort ohne Zwischenfragen heruntergeladen und installiert. Optionale Updates must du mit einem Klick auf "Install" bestätigen. Installiere auf jeden Fall auch alle optionalen Updates, wenn welche verfügbar sind.

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

### Guide -> Installieren der Rolle "Active Directory Domain Services"
#### Guide Overview
Dieser Guide zeigt dir wie die Rolle "Active Directory Domain Services" mit dem "Add Roles and Features Wizard" auf dem Server installierst.
#### Dauer:
ca 30 Minuten
#### Step1: Gehe zum "Add Roles and Features Wizard"

Sollte der "Server Manager" geschlossen sein so öffne diesen bitte. Solltest du nicht wissen wie, siehe bitte unter [Server Manager über das Startmenü starten](#server-manage-über-das-startmenü-starten) oder [Server Manager über die Suchleiste starten](#server-manager-über-die-suchleiste-starten) nach wie der "Server Manager" geöffnet wird.
Klicke auf "Manage" und wähle danach "Add Roles and Features" um zum "Add Roles and Features Wizard" zu gelagen.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_go_to_roles_wizard.png)

#### Step2: Füge die Rolle "Active Directory Domain Services" dem Server hinzu

Klicke auf "Next"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_start.png)

Wähle im nächsten Schritt "Role-based or feature-based installation" und Klicke anschließend auf "Next".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_select_install_type.png)

Wähle unter "Server Selection" die Option "Select a server from the server pool" und danach deinen Server aus. Anschließend klicke auf "Next"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_select_server.png)

Wähle nun die Rolle "Active Directory Domain Services". Klicke hierfür das Kästchen vor dem Rollennamen.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_add_role_active_directory.png)

Bestätige das Hinzufügen der Rolle mit einem Klick auf "Add Features"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_add_role_active_directory_confirm_add.png)

Klicke auf "Next"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_server_roles_active_directory_finish.png)

Für die Installation des Active Directories werden keine weiteren Features benötigt. Daher können wir hier einfach auf "Next klicken"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_server_features.png)

Im Nächsten Fenster bekommen wir noch eine Zusammenfassung zu den "Active Directory Domain Services". Klicke auch hier wieder auf "Next"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_active_directory_information.png)

Als nächstes bekommen wir eine Zusammenfassung der Rollen und Features die mit einem Klick auf "Install" installiert werden. Wähle davor jedoch die Option "Restart the destination server automatically if required" an.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_active_directory_confirmation.png)

Warte bis die ausgewählten Rollen und Features installiert sind.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_active_directory_installation.png)

Sobald alles fertig ist, schließe den "Add Roles and Features Wizard" durch einen Klick auf "Close".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_roles_wizard_active_directory_finish.png)

Jetzt solltest du mit der Konfiguration des Services fortfahren. Da wir hier die Rolle "Active Directory Domain Services" installiert haben, solltest mit [Promote Server to a Domain Controller](https://) weitermachen.

###### [Index](#Index)

---

### Guide -> Promoten des Servers zu einem Active Directory Domain Controller
#### Guide Overview
Dieser Guide erklärt wie nach der Installation der Roll "Active Directory Domain Services", der Server zu einem Domaincontroller hochgestuft wird.
#### Dauer:
ca 30 Minuten
#### Step1: Gehe zum "Active Directory Domain Services Configuration Wizard" 
Klicke rechts oben auf das Flaggen Symbol welches für "Notifications" steht und anschließend auf "Promote this server to a domain controller".

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_promote_ad_start.png)

#### Step2: Deployment Configuration

Wähle im nächsten Fenster "Add a new forest" und gibt deinen gewünschten "root domain name" ein. Im Falle dieses Tutorials is der "root domain name" "kerberos.doku.owncloud.works".
Danach klicke auf "Next"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_promote_ad_deployment_configuration.png)

#### Step3: Domain Controller Options

Vergebe ein sicheres Passwort, notiere es dir und gib es danach in die beiden Felder "Password" und "Confirm password" ein und ein Password für den "Directory Services Restore Mode" (DSRM) zu vergeben.

Der Verzeichnisdienste -Wiederherstellungsmodus (Directory Service Restore Mode) ist eine sichere Boot-Option für Windows-Server-Domänencontroller. DSRM ermöglicht es einem Administrator, eine Active-Directory-Datenbank zu reparieren oder wiederherzustellen. 

Wenn die Binärdateien des Active Directory installiert sind, fordert der Installationsassistent beim Heraufstufen eines Servers zum Domänencontroller den Administrator auf, ein DSRM-Kennwort zu wählen. Dieses Kennwort bietet dem Administrator eine Hintertür in die Datenbank für den Fall, dass später etwas schief geht und eine Wiederherstellung notwendig ist. Der Modus bietet aber keinen Zugriff auf die Domäne oder irgendwelche Serverdienste. Für den Fall, dass Administartoren ein DSRM-Kennwort vergessen, kann es mit dem Kommandozeilen-Tool NTDSUtil geändert werden.

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_promote_ad_dsrm.png)

#### Step3: DNS Options

Hier müssen wir nichts ändern und können einfach auf next klicken.


![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_promote_dns_options.png)

#### Step4: Additional Options

Auch hier müssen wir nichts machen. Im Feld "The NetBIOS domain name" sollte der erste teile der domain in Großbuchstaben stehen. Im Falle des Tutorials wo der "root domain name" "kerberos.doku.owncloud.works" ist, sollte nun im Feld "KERBEROS" stehen.

Sollte dies nicht der Fall sein so muss bei der Konfiguration im Vorfeld ein Fehler aufgetreten sein.

Auch hier klicken wir wieder auf "Next" wenn alles passt.
 
![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_promote_ad_additional_options.png)

#### Step5: Paths

Sollten die Dateien für Datenbank, Logfile und dem "SYSVOL" geändert werden so muss dies hier gemacht werden. Es wird jedoch empfohlen die voreingestellten Pfade zu nutzen.

klicke hier einfach auf "Next"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_promote_paths.png)

#### Step6: Review Options

Im nächsten Fenster kannst du noch einmal alle Einstellungen die gesetzt wurden überprüfen. Sollte alles passen klicke auf "Next" 

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_promote_review_options.png)

#### Step6: Prerequisites Check

Hier werden noch einmal alle Einstellungen die gesetzt wurden auf ihre Richtigkeit geprüft. Ignoriere die gelben "Warnings". Diese haben auf das hoch Stufen des Servers keinen Einfluss. 

Sollten alle Checks erfolgreich abgeschlossen sein, so klicke auf "Install"

![image](https://github.com/GeraldLeikam/tutorials/blob/master/images/windows/server/server_manager/windows_server_2022_server_manager_promote_prerequisites_check.png)
