# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| aws | n/a |
| template | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| FMC\_version | specified FMC version. | `string` | `"fmcv-7.1.0"` | no |
| FTD\_version | specified FTD version. | `string` | `"ftdv-7.1.0"` | no |
| availability\_zone\_count | Spacified availablity zone count . | `number` | `2` | no |
| create\_fmc | Boolean value to create FMC or not | `bool` | `true` | no |
| fmc\_admin\_password | spacified fmc admin password . | `string` | `"Cisco@123"` | no |
| fmc\_hostname | spacified fmc hostname . | `string` | `"FMC-01"` | no |
| fmc\_mgmt\_ip | specified fmc management IPs . | `string` | `""` | no |
| fmc\_nat\_id | specified fmc nat id . | `string` | `""` | no |
| fmcmgmt\_interface | spacified ftd management interface . | `string` | `""` | no |
| ftd\_diag\_interface | list out ftd digonstic interface . | `list(string)` | `[]` | no |
| ftd\_inside\_interface | list out ftd inside interface . | `list(string)` | `[]` | no |
| ftd\_mgmt\_interface | list out ftd management interface . | `list(string)` | `[]` | no |
| ftd\_outside\_interface | list out ftd outside interface . | `list(string)` | `[]` | no |
| ftd\_size | specified server instance type . | `string` | `"c5.4xlarge"` | no |
| instances\_per\_az | Spacified no. of instance per az wants to be create . | `number` | `1` | no |
| keyname | specified key pair name to connect firewall . | `string` | n/a | yes |
| reg\_key | spacified reg key . | `string` | `"cisco"` | no |
| tags | map the required tags . | `map` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| instance\_private\_ip | Public IP address of the EC2 instance |
| instance\_public\_ip | Public IP address of the EC2 instance |

<!--- END_TF_DOCS --->
