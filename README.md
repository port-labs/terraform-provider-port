[DEPRECATED]

This is the old version of Port's Terraform provider and is no longer maintained. To use Terraform to manage your Port account, please use the [new Terraform provider](https://docs.getport.io/build-your-software-catalog/sync-data-to-catalog/iac/terraform/) and look at the [terraform-provider-port-labs](https://github.com/port-labs/terraform-provider-port-labs) repository.

You can also view the up to date version of Port's Terraform provider in the [Terraform registry](https://registry.terraform.io/providers/port-labs/port-labs/latest)

<img align="right" src="https://user-images.githubusercontent.com/8277210/183290078-f38cdfd2-e5da-4562-82e6-f274d0330825.svg#gh-dark-mode-only" width="100" height="74" /> <img align="right" width="100" height="74" src="https://user-images.githubusercontent.com/8277210/183290025-d7b24277-dfb4-4ce1-bece-7fe0ecd5efd4.svg#gh-light-mode-only" />

# Port Terraform Provider

[![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)](https://join.slack.com/t/devex-community/shared_invite/zt-1bmf5621e-GGfuJdMPK2D8UN58qL4E_g)


Port is the Developer Platform meant to supercharge your DevOps and Developers, and allow you to regain control of your environment.

### Docs
* [Provider Docs](https://registry.terraform.io/providers/port-labs/port/latest/docs)
* [Port Docs](https://docs.getport.io/)

## Installation

```terraform
terraform {
  required_providers {
    port = {
      source  = "port-labs/port"
      version = "~> 0.0.1"
    }
  }
}
provider "port" {}

resource "port_entity" "microservice" {
  title     = "monolith"
  blueprint = "microservice_blueprint"
  properties {
    name  = "microservice_name"
    value = "golang_monolith"
    type  = "string"
  }
}
```
