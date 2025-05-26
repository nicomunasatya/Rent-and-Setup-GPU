# Rent-and-Setup-GPU
Steps guide to rent, setup and config connect from GPU servers

# Step 1. Create a Public SSH using PowerShell
### 1- Open Windows PowerShell or WSL Ubuntu Terminal
In Windows Start Menu, Find **Windows PowerShell**, Right click on it and click on **Run as Administrator**.

### 2- In the terminal run:
```bash
ssh-keygen -t rsa -b 4096
```
* You'll see:
```
Generating public/private rsa key pair.
Enter file in which to save the key (C:\Users\YourUsername\.ssh\id_rsa):
```
* Press `Enter` to accept the default location.

```
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
```
* Press `Enter` to bypass setting password.

### 3- Navigate to `.ssh` directory
```
cd $env:USERPROFILE\.ssh
```
### 4- Copy the `id_rsa.pub` file content in clipboard
```
Get-Content id_rsa.pub | Set-Clipboard
```
* Your public key is now copied into your `clipboard`
