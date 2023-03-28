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
| diagnostic\_subnet | diagnostic newtwork subnet | `string` | `""` | no |
| image\_version | Version of the FTDv | `string` | `"710.3.0"` | no |
| inside\_subnet | Inside newtwork subnet | `string` | `""` | no |
| instancename | FTDv instance Name | `string` | `"FTDv"` | no |
| instances | Number of FTDv instances | `number` | `2` | no |
| location | Azure region | `string` | `"eastus2"` | no |
| management\_subnet | Management newtwork subnet | `string` | `""` | no |
| outside\_subnet | Outside newtwork subnet | `string` | `""` | no |
| password | Password for the VM OS | `string` | `"P@$$w0rd1234"` | no |
| prefix | Prefix to prepend resource names | `string` | `"cisco-FTDv"` | no |
| rg\_name | Azure Resource Group | `string` | `"cisco-FTDv-RG"` | no |
| source\_address | Limit the Management access to specific source | `string` | `"*"` | no |
| username | Username for the VM OS | `string` | `"cisco"` | no |
| vm\_size | Size of the VM for ASAv | `string` | `"Standard_D3_v2"` | no |
| vn\_name | Existing Virtual Network Name | `string` | `""` | no |

## Outputs

| Name | Description |
|------|-------------|
| FTDv\_Instance\_Public\_IPs | n/a |

<!--- END_TF_DOCS --->
