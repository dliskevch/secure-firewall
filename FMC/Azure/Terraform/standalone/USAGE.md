# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| azurerm | =2.65.0 |

## Providers

| Name | Version |
|------|---------|
| azurerm | =2.65.0 |
| random | n/a |
| template | n/a |
| tls | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| fmc\_virtual\_machine\_name | FMC in Azure | `string` | n/a | yes |
| linux\_virtual\_machine\_name | Linux VM in Azure | `string` | n/a | yes |
| network\_interface\_fmc | FMC NIC in Azure | `string` | n/a | yes |
| network\_interface\_name | NIC OS in Azure | `string` | n/a | yes |
| network\_interface\_win | NIC Win10 in Azure | `string` | n/a | yes |
| network\_security\_group\_ALL | NSG Default in Azure | `string` | n/a | yes |
| network\_security\_group\_VM | NSG VM in Azure | `string` | n/a | yes |
| public\_ip\_fmc | Public IP FMC in Azure | `string` | n/a | yes |
| public\_ip\_ubuntu | Public IP OS in Azure | `string` | n/a | yes |
| public\_ip\_win | Public IP Win10 in Azure | `string` | n/a | yes |
| resource\_group\_location | RG location in Azure | `string` | n/a | yes |
| resource\_group\_name | RG name in Azure | `string` | n/a | yes |
| subnet\_name\_1 | Subnet 1 in Azure | `string` | n/a | yes |
| subnet\_name\_2 | Subnet 2 in Azure | `string` | n/a | yes |
| subnet\_name\_3 | Subnet 3 in Azure | `string` | n/a | yes |
| subnet\_name\_4 | Subnet 4 in Azure | `string` | n/a | yes |
| virtual\_network\_name | VNET name in Azure | `string` | n/a | yes |
| win\_virtual\_machine\_name | Win10 in Azure | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| fmc\_id | n/a |
| public\_ip\_address\_Ubuntu | n/a |
| public\_ip\_address\_fmcv | n/a |
| public\_ip\_address\_win10 | n/a |
| tls\_private\_key | n/a |
| vm\_id | n/a |
| win\_id | n/a |

<!--- END_TF_DOCS --->
