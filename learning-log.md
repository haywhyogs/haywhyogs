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