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
| admin\_password | password for admin | `string` | n/a | yes |
| admin\_ssh\_pub\_key | ssh public key for admin | `string` | n/a | yes |
| compartment\_id | compartment id where to create all resources | `string` | n/a | yes |
| day\_0\_config | Render a startup script with a template. | `string` | `"startup_file.json"` | no |
| diag\_network | diag network name | `string` | `""` | no |
| dmz\_network | dmz network name | `string` | `""` | no |
| fingerprint | n/a | `any` | n/a | yes |
| hostname | FTD hostname | `string` | `"cisco-ftd"` | no |
| inside\_network | inside network name | `string` | `"vpc-inside"` | no |
| label\_prefix | a string that will be prepended to all resources | `string` | `"ftd"` | no |
| mgmt\_network | management network name | `string` | `""` | no |
| mp\_listing\_resource\_id | Marketplace Listing Image OCID | `string` | `"ocid1.image.oc1..aaaaaaaamybyw5im3tfl5fimi3nd57no3mtczwenrll7fgkzi4zgbc32tlqa"` | no |
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
| network\_5\_external\_ip | n/a | `bool` | `false` | no |
| network\_5\_name | n/a | `string` | `""` | no |
| network\_5\_private\_ip | n/a | `list(string)` | `[]` | no |
| network\_5\_subnet\_cidr | n/a | `string` | `""` | no |
| network\_5\_vcn\_cidr | n/a | `string` | `""` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| outside\_network | outside network name | `string` | `""` | no |
| private\_key\_path | n/a | `any` | n/a | yes |
| region | the OCI region where resources will be created | `string` | n/a | yes |
| tenancy\_ocid | ########################### Provider Configuration  # ########################### | `string` | n/a | yes |
| user\_ocid | n/a | `any` | n/a | yes |
| vm\_compute\_shape | Compute Shape | `string` | `"VM.Standard2.8"` | no |

## Outputs

| Name | Description |
|------|-------------|
| networks\_list | A list of network related info such as name, links,subnet links, cidr, internal IP, has external IP or not etc |
| vm\_external\_ips | external ips for created instances. |
| vm\_private\_ips | Private IPs of created instances. |

<!--- END_TF_DOCS --->
