# Guide -> Install scp command on a ubuntu machine

## Guide Overview
This guide will show you how to install the ```scp``` command on a machine/server running the Ubuntu/Debian operating system.

## Step1: Update System
Update your package lists and download the latest upgrades:
```bash
apt update && apt upgrade -y
```
## Step2: Install scp command
```bash
apt install -y openssh-client
```
Congratulations, the ```scp``` command is now available on this system.