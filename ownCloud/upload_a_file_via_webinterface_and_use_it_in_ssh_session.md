# Guide -> Upload a file via ownCloud web interface and use it in terminal

## Guide Overview
This guide aims to demonstrate how to upload a file through the ownCloud web interface and then use it in an SSH session in the terminal. This can be very helpful when you want to upload configuration files to the server that are required by a specific service.

In the scenario of this guide, we want to upload a configuration file called ```ultra.conf``` using the ```admin``` user to the server ```cloud.tutorial.owncloud.works``` in the ```/Uploads``` folder. After the upload, we will copy the file to ```/etc/ultra/ultra.conf``` through an SSH connection using the terminal.
## Step1: Upload file
Please log in to your ownCloud through your web browser, preferably using the admin user. Create a folder where you can upload your files. If you prefer not to create a new folder, you can upload files to an existing folder or directly to the root directory.
## Step2: Work on Terminal with it
### Login in via SSH
[Please log in to your ownCloud server using SSH]
```bash
ssh root@cloud.tutorial.owncloud.works
```
### Navigate to file 
Please navigate to the "files" directory of the user you are using.
```bash
cd /var/www/owncloud/data/<<user>>/files
```
in our case: 
```bash
cd /var/www/owncloud/data/admin/files/Uploads
```
### Copy file to new destination
It is important to use cp to copy the files and not mv. Moving files with mv can cause errors in the database and affect the functionality of ownCloud.

in our case:
```bash
cp ultra.conf /etc/ultra/ultra.conf
```
If necessary, [adjust the permissions] of the file or [change the owner and group].


[Please log in to your ownCloud server using SSH]: https://github.com/GeraldLeikam/tutorials/blob/master/
[adjust the permissions]: https://github.com/GeraldLeikam/tutorials/blob/master/
[change the owner and group]: https://github.com/GeraldLeikam/tutorials/blob/master/