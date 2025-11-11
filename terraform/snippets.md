## Useful Terraform Snippets

**Main.tf sample:**
```hcl
terraform {
  required_providers {
    azurerm = {
      source  = "hashicorp/azurerm"
      version = "~> 3.0.2"
    }
  }

  required_version = ">= 1.1.0"
}

provider "azurerm" {
  features {}
}

resource "azurerm_resource_group" "rg" {
  name     = var.resource_group_name
  location = var.location
}

```
**Variables.tf sample**
```
variable "resource_group_name" {
  default = "myTFResourceGroup"
}

variable "location" {
  default = "canadacentral"
}
```
## Common Commands
- terraform init – initializes the working directory and downloads providers.

- terraform fmt – formats the Terraform files.

- terraform validate – checks configuration syntax and validity.

- terraform apply – creates or updates infrastructure.

- terraform show – displays current state or plan details.

- terraform state list – lists all managed resources.

- terraform state show <resource> – shows details of a specific resource.