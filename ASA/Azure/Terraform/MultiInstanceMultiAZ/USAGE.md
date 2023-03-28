# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| azurerm | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| azs | Azure Availability Zones | `list` | <pre>[<br>  "1",<br>  "2",<br>  "3"<br>]</pre> | no |
| create\_rg | Wheather to create Resource Group | `bool` | `true` | no |
| create\_vn | Wheather to create Virtual Network | `bool` | `true` | no |
| image\_version | Version of the ASAv | `string` | `"917.0.3"` | no |
| instancename | ASAv instance Name | `string` | `"ASAv"` | no |
| instances | Number of ASAv instances | `number` | `2` | no |
| location | Azure region | `string` | `"eastus2"` | no |
| password | Password for the VM OS | `string` | `"P@$$w0rd1234"` | no |
| prefix | Prefix to prepend resource names | `string` | `"cisco-ASAv"` | no |
| rg\_name | Azure Resource Group | `string` | `"cisco-ASAv-RG"` | no |
| source\_address | Limit the Management access to specific source | `string` | `"*"` | no |
| subnet\_size | Size of Subnets | `number` | `24` | no |
| subnets | subnets for FTD interfaces | `list` | `[]` | no |
| username | Username for the VM OS | `string` | `"cisco"` | no |
| vm\_size | Size of the VM for ASAv | `string` | `"Standard_D3_v2"` | no |
| vn\_cidr | Virtual Network CIDR | `string` | `"10.0.0.0/16"` | no |
| vn\_name | Existing Virtual Network Name | `string` | `""` | no |

## Outputs

| Name | Description |
|------|-------------|
| ASAv\_Instance\_Public\_IPs | n/a |

<!--- END_TF_DOCS --->
