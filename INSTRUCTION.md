# terraform-azurerm-resource_group_storage

Terraform module that creates an Azure Resource Group and a Storage Account inside it.

## Usage

```hcl
module "resource_group_storage" {
  source  = "spridoloba/resource_group_storage/azurerm"
  version = "1.0.0"

  resource_group_name  = "my-resource-group"
  location             = "East US"
  storage_account_name = "mystorageaccount123"
}
```

## Inputs

| Name | Description | Type | Required |
|------|-------------|------|----------|
| resource_group_name | Name of the resource group | string | yes |
| location | Azure region | string | yes |
| storage_account_name | Name of the storage account | string | yes |

## Outputs

| Name | Description |
|------|-------------|
| resource_group_id | ID of the created resource group |
| storage_account_id | ID of the created storage account |

## Requirements

- Terraform >= 1.0
- AzureRM provider ~> 3.0
- Azure subscription with appropriate permissions
