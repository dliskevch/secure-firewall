# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| terraform | >=1.0.0 |

## Providers

No provider.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| admin\_password | password for admin | `string` | n/a | yes |
| admin\_ssh\_pub\_key | ssh public key for admin | `any` | n/a | yes |
| cisco\_product\_version | cisco product version | `string` | `"cisco-ftdv-7-0-0-94"` | no |
| day\_0\_config | Render a startup script with a template. | `string` | `""` | no |
| diag\_network | diag network name | `string` | `""` | no |
| dmz\_network | dmz network name | `string` | `""` | no |
| hostname | FTD hostname | `string` | `"ftd"` | no |
| inside\_network | inside network name | `string` | `""` | no |
| mgmt\_network | management network name | `string` | `""` | no |
| networks | a list of VPC | `list(object({ name = string, cidr = string, appliance_ip = list(string), external_ip = bool }))` | `[]` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| outside\_network | outside network name | `string` | `""` | no |
| project\_id | The project ID to host the network in | `any` | n/a | yes |
| region | The region | `any` | n/a | yes |
| vm\_instance\_labels | Labels to apply to the vm instances. | `map(string)` | `{}` | no |
| vm\_instance\_tags | Additional tags to apply to the instances, please note the service account is used as much as possible as best practice | `list(string)` | `[]` | no |
| vm\_machine\_type | machine type for appliance | `string` | `"e2-standard-4"` | no |
| vm\_zones | The zones | `list(string)` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| networks\_list | list of networks |
| vm\_external\_ips | external ips for VPC networks |

<!--- END_TF_DOCS --->
