## 2025-09-01
- Cloned README repo and edited via VS Code on WSL.
- Pushed edits from VS Code terminal to GitHub.

## 2025-09-13
- Wrote and passed the AZ-900 Exam

## 2025-09-20
### Azure CLI Installation and Setup
- Installed and used Azure CLI in WSL.
- Practiced basic shell commands and created linux/README.md and linux/snippets.md.
- Installed the Azure CLI 
- Updated the Azure CLI to the latest version.
- Signed in with my student account using `az login` and verified successful authentication.
- Confirmed that the CLI is working correctly and connected to my Azure account.
## 2025-09-27
### Terraform Installation & Setup
- Installed `gnupg` and `software-properties-common` packages.
- Added the official HashiCorp repository and installed Terraform.
- Verified installation using `terraform -version`.

- Created `main.tf` and configured Azure provider.
- Used Azure CLI to authenticate instead of a Service Principal.

**Azure Authentication Challenge & Lesson Learned**

*Because I’m using a student subscription, I don’t have the permissions required to create a Service Principal (which typically requires Azure AD admin or contributor rights). At first, this almost got a bit frustrating — not exactly frustration, but the moment made me pause to understand why it wasn’t working.*

*After doing some research, I learned that:*
* *Permissions and access control are fundamental in cloud environments.*

* *Certain Azure operations (like creating Service Principals or managing app registrations) are restricted under specific account types, especially student or limited subscriptions.*

* *I could bypass this by authenticating through the Azure CLI instead, using my logged-in credentials (az login), which Terraform can automatically detect.*

*This workaround not only helped me continue the tutorial but also gave me a deeper understanding of how identity and access management (IAM) plays a crucial role in cloud security and automation.*
- Commands learned: `terraform init`, `fmt`, `validate`, `apply`, `show`, `state list`, `state show`.
## 2025-10-03
### SSH with Azure VMs

- Created a Virtual Machine using the Azure Portal.
- Selected the desired **Availability Zone**.
- Enabled **SSH** as the authentication method.
- Configured **inbound port 22** for SSH access.
- Copied the VM's **public IP address**.
- Downloaded the `.pem` private key to my computer for authentication.

### Connecting via VS Code
- Installed the **Remote - SSH** extension.
- Added a new host using the following format:
```text
ssh user@hostname -i /privatekey filepath
```

* user = username created when adding the SSH public key to VM (default is azureuser)

* hostname = Public IP address of the VM

* filepath = path to the downloaded .pem private key

* Successfully connected to the VM.

### Run and Debug Code
* Updated Linux packages on VM and installed Node.js.
* Installed Express generator and created a new Express app. Ran `npm install` and started the server. Forwarded port 3000 to check the web app locally.
* Opened the app in VS Code, set a breakpoint on line 10, and successfully debugged the application remotely. 
* Learned how I can seamlessly develop on a remote machine via SSH.

## 2025-10-10
### Linux Basics
- listed / hidden files
- searching / filtering using grep
- file size analysis
- user & permission investigation
- daily challenge tasks to build muscle memory