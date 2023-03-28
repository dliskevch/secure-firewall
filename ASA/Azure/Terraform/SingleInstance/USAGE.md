# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| azurerm | =2.56.0 |

## Providers

| Name | Version |
|------|---------|
| azurerm | =2.56.0 |
| template | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| IPAddressPrefix | n/a | `string` | `"10.10"` | no |
| RGName | n/a | `string` | `"cisco-asav-RG"` | no |
| VMSize | n/a | `string` | `"Standard_D3_v2"` | no |
| Version | n/a | `string` | `"915.1.1"` | no |
| day-0-config | n/a | `string` | `"ASA_Running_Config.txt"` | no |
| instancename | n/a | `string` | `"cisco-asav"` | no |
| instancepassword | n/a | `string` | `"Pa$$w0rd1234"` | no |
| instanceusername | n/a | `string` | `"cisco"` | no |
| location | n/a | `string` | `"westeurope"` | no |
| prefix | n/a | `string` | `"cisco-asav"` | no |
| source-address | n/a | `string` | `"*"` | no |

## Outputs

| Name | Description |
|------|-------------|
| public\_ip\_address | n/a |

<!--- END_TF_DOCS --->
