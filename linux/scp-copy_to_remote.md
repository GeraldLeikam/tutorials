# Guide -> Copy Files via scp to a remote host (key authentication)

## Guide Overview
Dieser Guide erklärt dir wie du mit scp dateien/ordner auf einen remote Server kopierst. Für dieses Tutorial verwenden wird die Key Authentifizierungs Methode. 
In dem Szenario für diesen Guide möchten wir eine Datei -> /home/user/Downloads/demo.dat und einen Ordner mit 
Unterornern -> /home/user/data_to_move/ auf einen remote Server mit der fiktiven ip 178.56.24.12 kopieren. 

## Step1: Verify scp is installed
Verfiziere das das scp kommando auf deinem rechner verfügbar ist: 
```bash
which scp
```
Der output des kommandos sollte wie folgend aussehen:
```bash
/usr/bin/scp
```
If no output is displayed, it means that scp is not installed and needs to be installed first. [You can learn how to install scp here]
## Step1: Navigate to source file/directory
Navigiere zum Speicherort der Datei:
```bash
cd /home/user/Downloads/
```
Navgiere zum Speicherotz des Ornders:
```bash
cd /home/user/
```

## Step2: Copy file/directory to remote Server


[You can learn how to install scp here]: https://github.com/GeraldLeikam/tutorials/blob/master/linux/install_scp_command_unbuntu.md