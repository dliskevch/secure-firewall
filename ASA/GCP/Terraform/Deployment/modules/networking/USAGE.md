# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| terraform | >=1.0.3 |
| google | ~> 3.79, <4.0 |

## Providers

| Name | Version |
|------|---------|
| google | ~> 3.79, <4.0 |
| random | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| custom\_route\_tag | tag for custom route | `string` | n/a | yes |
| dmz1\_network | dmz1 network name | `string` | n/a | yes |
| dmz2\_network | dmz2 network name | `string` | n/a | yes |
| ha\_enabled | HA enabled | `bool` | `false` | no |
| inside\_network | inside network name | `string` | n/a | yes |
| mgmt\_network | management network name | `string` | n/a | yes |
| networks | a list of VPC | `list(object({ name = string, cidr = string, appliance_ip = list(string), external_ip = bool }))` | `[]` | no |
| outside\_network | outside network name | `string` | n/a | yes |
| project\_id | The project ID to host the network in | `any` | n/a | yes |
| region | The region | `any` | n/a | yes |
| service\_account | The email address of the service account which will be assigned to the compute instances. | `string` | n/a | yes |
| service\_port | service port | `number` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| networks\_list | A list of network related info such as name, links,subnet links, cir, internal IP, has external IP or not etc |
| networks\_map | A map of network related info such as name, links,subnet links, cir, internal IP, has external IP or not etc |

<!--- END_TF_DOCS --->
