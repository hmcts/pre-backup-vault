# pre-backup-vault

Module for creating a backup vault and associated resurces. https://learn.microsoft.com/en-us/azure/backup/backup-vault-overview

<!-- BEGIN_TF_DOCS -->


## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | n/a |

## Resources

| Name | Type |
|------|------|
| [azurerm_data_protection_backup_instance_blob_storage.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/data_protection_backup_instance_blob_storage) | resource |
| [azurerm_data_protection_backup_policy_blob_storage.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/data_protection_backup_policy_blob_storage) | resource |
| [azurerm_data_protection_backup_vault.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/data_protection_backup_vault) | resource |
| [azurerm_resource_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/resource_group) | resource |
| [azurerm_role_assignment.backup_contributor](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/role_assignment) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_env"></a> [env](#input\_env) | n/a | `any` | n/a | yes |
| <a name="input_location"></a> [location](#input\_location) | n/a | `any` | n/a | yes |
| <a name="input_location_backup"></a> [location\_backup](#input\_location\_backup) | n/a | `string` | `"UK West"` | no |
| <a name="input_product"></a> [product](#input\_product) | n/a | `any` | n/a | yes |
| <a name="input_retention_duration"></a> [retention\_duration](#input\_retention\_duration) | n/a | `any` | n/a | yes |
| <a name="input_rg_name"></a> [rg\_name](#input\_rg\_name) | n/a | `any` | n/a | yes |
| <a name="input_role_assignments"></a> [role\_assignments](#input\_role\_assignments) | List of roles to assign to the provided Managed Identity | `list(string)` | <pre>[<br>  "Storage Account Backup Contributor"<br>]</pre> | no |
| <a name="input_storageaccount_ids"></a> [storageaccount\_ids](#input\_storageaccount\_ids) | List of storage accounts to take a backup of | `list(string)` | `[]` | no |
| <a name="input_tags"></a> [tags](#input\_tags) | n/a | `map(string)` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_resource_group_id"></a> [resource\_group\_id](#output\_resource\_group\_id) | The backup resource group name. |
| <a name="output_resource_group_name"></a> [resource\_group\_name](#output\_resource\_group\_name) | The backup resource group Resource ID. |
<!-- END_TF_DOCS -->