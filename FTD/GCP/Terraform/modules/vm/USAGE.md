# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| google | n/a |
| random | n/a |
| template | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| admin\_password | password for ftd admin | `string` | n/a | yes |
| admin\_ssh\_pub\_key | ssh public key for admin | `string` | n/a | yes |
| cisco\_product\_version | cisco product version | `string` | `"cisco-ftdv-7-0-0-94"` | no |
| custom\_route\_tag | tag for custom route | `string` | n/a | yes |
| day\_0\_config | zero day configuration | `string` | `""` | no |
| hostname | FTD hostname | `string` | `"ftd"` | no |
| mgmt\_network | management network name | `string` | `""` | no |
| networks\_list | network links in a map(network\_name) | `list(object({ name = string, network_self_link = string, subnet_self_link = string, subnet_cidr = string, appliance_ip = list(string), external_ip = bool, routes = list(string) }))` | n/a | yes |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| project\_id | The project ID to host the network in | `string` | n/a | yes |
| region | The region | `string` | n/a | yes |
| service\_account | The email address of the service account which will be assigned to the compute instances. | `string` | n/a | yes |
| vm\_instance\_labels | Labels to apply to the vm instances. | `map(string)` | `{}` | no |
| vm\_instance\_tags | Additional tags to apply to the instances, please note the service account is used as much as possible as best practice | `list(string)` | `[]` | no |
| vm\_machine\_type | machine type for appliance | `string` | `"e2-standard-4"` | no |
| vm\_zones | The zones | `list(string)` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| external\_ips | external ips for VPC networks |
| instance\_ids | a list of instance ids |

<!--- END_TF_DOCS --->
