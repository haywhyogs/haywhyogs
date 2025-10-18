# Learning SSH with Azure VMs

## Overview
This folder documents my progress learning SSH and securely connecting to Azure Virtual Machines (VMs) using VS Code.

## Prerequisites
- Azure account
- Basic knowledge of Linux commands
- VS Code installed
- Remote - SSH extension installed in VS Code
- OpenSSH client installed on local machine

## Steps Completed

### 1. Create Azure VM with SSH
- I Created a Virtual Machine using the Azure Portal.
- Selected the desired **Availability Zone**.
- Enabled **SSH** as the authentication method.
- Configured **inbound port 22** for SSH access.
- Copied the VM's **public IP address**.
- Downloaded the `.pem` private key to my computer for authentication.

### 2. Connecting via VS Code
- Installed the **Remote - SSH** extension.
- Added a new host using the following format:
```text
ssh user@hostname -i /path/to/private_key.pem
