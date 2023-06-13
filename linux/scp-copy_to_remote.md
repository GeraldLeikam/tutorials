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
The scp command syntax take the following form:
```bash
scp [OPTION] [user@]SRC_HOST:]file1 [user@]DEST_HOST:]file2
```
- ```OPTION``` - scp options such as cipher, ssh configuration, ssh port, limit, recursive copy …etc.
- ```[user@]SRC_HOST:]file1``` - Source file.
- ```[user@]DEST_HOST:]file2``` - Destination file

Local files should be specified using an absolute or relative path, while remote file names should include a user and host specification.

```scp``` provides a number of options that control every aspect of its behavior. The most widely used options are:

- ```-P``` - Specifies the remote host ssh port.
- ```-p``` - Preserves files modification and access times.
- ```-q``` - Use this option if you want to suppress the progress meter and non-error messages.
- ```-C``` - This option forces scp to compresses the data as it is sent to the destination machine.
- ```-r``` - This option tells scp to copy directories recursively.

Understood the command? Alright, let's proceed with the copying process:
kopiere datei:
```bash
scp demo.dat yourusername@178.56.24.12:/remote/directory
```
kopiere Ordner
```bash
scp -r data_to_move remote_username@10.10.0.2:/remote/directory
```




[You can learn how to install scp here]: https://github.com/GeraldLeikam/tutorials/blob/master/linux/install_scp_command_unbuntu.md