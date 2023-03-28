# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| terraform | >=1.0.0 |
| oci | ~> 4.46.0 |

## Providers

No provider.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| admin\_ssh\_pub\_key | ssh public key for admin | `string` | n/a | yes |
| compartment\_id | compartment id where to create all resources | `string` | n/a | yes |
| day\_0\_config | Render a startup script with a template. | `string` | `""` | no |
| dmz1\_network | dmz1 network name | `string` | `""` | no |
| dmz2\_network | dmz2 network name | `string` | `""` | no |
| enable\_password | enable password for ASA zero day config | `string` | n/a | yes |
| fingerprint | n/a | `any` | n/a | yes |
| inside\_network | inside network name | `string` | `"vpc-inside"` | no |
| label\_prefix | a string that will be prepended to all resources | `string` | `"none"` | no |
| mgmt\_network | management network name | `string` | `""` | no |
| mp\_listing\_resource\_id | Marketplace Listing Image OCID | `string` | `"ocid1.image.oc1..aaaaaaaapbmcovv6mtuhpllezyzcpew2jysqnnqj6maij53qefxm3ugjuhcq"` | no |
| multiple\_ad | n/a | `bool` | `false` | no |
| network\_1\_external\_ip | n/a | `bool` | `false` | no |
| network\_1\_name | n/a | `any` | n/a | yes |
| network\_1\_private\_ip | n/a | `list(string)` | n/a | yes |
| network\_1\_subnet\_cidr | n/a | `any` | n/a | yes |
| network\_1\_vcn\_cidr | n/a | `any` | n/a | yes |
| network\_2\_external\_ip | n/a | `bool` | `false` | no |
| network\_2\_name | n/a | `any` | n/a | yes |
| network\_2\_private\_ip | n/a | `list(string)` | n/a | yes |
| network\_2\_subnet\_cidr | n/a | `any` | n/a | yes |
| network\_2\_vcn\_cidr | n/a | `any` | n/a | yes |
| network\_3\_external\_ip | n/a | `bool` | `false` | no |
| network\_3\_name | n/a | `any` | n/a | yes |
| network\_3\_private\_ip | n/a | `list(string)` | n/a | yes |
| network\_3\_subnet\_cidr | n/a | `any` | n/a | yes |
| network\_3\_vcn\_cidr | n/a | `any` | n/a | yes |
| network\_4\_external\_ip | n/a | `bool` | `false` | no |
| network\_4\_name | n/a | `any` | n/a | yes |
| network\_4\_private\_ip | n/a | `list(string)` | n/a | yes |
| network\_4\_subnet\_cidr | n/a | `any` | n/a | yes |
| network\_4\_vcn\_cidr | n/a | `any` | n/a | yes |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| outside\_network | outside network name | `string` | `""` | no |
| private\_key\_path | n/a | `any` | n/a | yes |
| region | the OCI region where resources will be created | `string` | n/a | yes |
| service\_port | service port | `number` | `80` | no |
| startup\_script | vm image | `string` | `""` | no |
| tenancy\_ocid | ########################### Provider Configuration  # ########################### | `string` | n/a | yes |
| user\_ocid | n/a | `any` | n/a | yes |
| vm\_compute\_shape | Compute Shape | `string` | `"VM.Standard2.4"` | no |

## Outputs

| Name | Description |
|------|-------------|
| external\_lb\_ip | The public ip address of the public load balancer |
| internal\_lb\_ip | The private  ip address of the private load balancer |
| networks\_list | A list of network related info such as name, links,subnet links, cidr, internal IP, has external IP or not etc |
| networks\_map | map of networks |
| vm\_external\_ips | external ips for created instances. |
| vm\_private\_ips | Private IPs of created instances. |

<!--- END_TF_DOCS --->
