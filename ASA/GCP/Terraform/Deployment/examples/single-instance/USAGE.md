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
| admin\_ssh\_pub\_key | ssh public key for admin | `any` | n/a | yes |
| cisco\_product\_version | cisco product version | `string` | `"cisco-asav-9-16-1-28"` | no |
| day\_0\_config | Render a startup script with a template. | `string` | `""` | no |
| dmz1\_network | dmz1 network name | `string` | `""` | no |
| dmz2\_network | dmz2 network name | `string` | `"vpc-dmz2"` | no |
| enable\_password | enable password for ASA zero day config | `string` | n/a | yes |
| inside\_network | inside network name | `string` | `""` | no |
| mgmt\_network | management network name | `string` | `""` | no |
| networks | a list of VPC | `list(object({ name = string, cidr = string, appliance_ip = list(string), external_ip = bool }))` | `[]` | no |
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
| network\_names | The names of the VPC networks being created |
| networks\_map | map of networks |
| vm\_external\_ips | external ips for VPC networks |

<!--- END_TF_DOCS --->
