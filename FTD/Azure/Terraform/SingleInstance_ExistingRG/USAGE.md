# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| azurerm | =2.53.0 |

## Providers

| Name | Version |
|------|---------|
| azurerm | =2.53.0 |
| template | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| VMSize | n/a | `string` | `"Standard_D3_v2"` | no |
| Version | n/a | `string` | `"700.94.0"` | no |
| diagnostic\_subnet | n/a | `string` | n/a | yes |
| inside\_subnet | n/a | `string` | n/a | yes |
| instancename | n/a | `string` | `"FTD01"` | no |
| location | n/a | `string` | `"centraleurope"` | no |
| management\_subnet | n/a | `string` | n/a | yes |
| outside\_subnet | n/a | `string` | n/a | yes |
| password | n/a | `string` | `""` | no |
| prefix | n/a | `string` | `"cisco-ftdv"` | no |
| rg\_name | n/a | `string` | n/a | yes |
| source-address | n/a | `string` | `"*"` | no |
| username | n/a | `string` | `""` | no |
| vn\_name | n/a | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| public\_ip\_address | n/a |

<!--- END_TF_DOCS --->
