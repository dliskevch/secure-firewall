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
| IPAddressPrefix | n/a | `string` | `"10.10"` | no |
| RGName | n/a | `string` | `"cisco-ftdv-RG"` | no |
| VMSize | n/a | `string` | `"Standard_D3_v2"` | no |
| Version | n/a | `string` | `"67065.0.0"` | no |
| instancename | n/a | `string` | `"FTD01"` | no |
| location | n/a | `string` | `"westeurope"` | no |
| password | n/a | `string` | `"P@$$w0rd1234"` | no |
| prefix | n/a | `string` | `"cisco-ftdv"` | no |
| source-address | n/a | `string` | `"*"` | no |
| username | n/a | `string` | `"cisco"` | no |

## Outputs

| Name | Description |
|------|-------------|
| public\_ip\_address | n/a |

<!--- END_TF_DOCS --->
