# Guide -> Install scp command on a ubuntu machine

## Guide Overview
Dieser Guide zeigt dir wie du das scp Kommando auf einem rechner/server mit ubuntu/debian Bertiebsystem installieren kannst.

## Step1: Update System
Upadte deine Packtlisten und lade die letzen upgrades herunter: 
```bash
apt update && apt upgrade -y
```
## Step2: Install scp command
```bash
apt install -y openssh-client
```
Herzlichen Glückwunsch das kommando scp ist jetzt in diesem system verfügbar