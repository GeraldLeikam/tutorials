# Guide -> Copy Files via scp to a remote host (key authentication)

## Guide Overview
This guide will explain how to use scp to copy files/folders to a remote server. For this tutorial, we will be using the key authentication method.

In the scenario for this guide, we want to copy a file -> /home/user/Downloads/demo.dat, and a folder with subdirectories -> /home/user/data_to_move/, to a remote server with the fictional IP address 178.56.24.12.

## Step1: Verify scp is installed
Please verify that the scp command is available on your machine by executing the following command:
```bash
which scp
```
The output of the command should look like the following:
```bash
/usr/bin/scp
```
If no output is displayed, it means that scp is not installed and needs to be installed first. [You can learn how to install scp here]
## Step1: Navigate to source file/directory
Please navigate to the location where the file is stored.
```bash
cd /home/user/Downloads/
```
Please navigate to the location where the folder is stored.
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

Copy file:
```bash
scp demo.dat yourusername@178.56.24.12:/remote/directory
```
copy folder:
```bash
scp -r data_to_move remote_username@10.10.0.2:/remote/directory
```




[You can learn how to install scp here]: https://github.com/GeraldLeikam/tutorials/blob/master/linux/install_scp_command_unbuntu.md