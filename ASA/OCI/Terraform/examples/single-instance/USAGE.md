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
| compartment\_id | compartment id where to create all resources | `string` | n/a | yes |
| day\_0\_config | Render a startup script with a template. | `string` | `""` | no |
| dmz1\_network | dmz1 network name | `string` | `""` | no |
| dmz2\_network | dmz2 network name | `string` | `"vpc-dmz2"` | no |
| enable\_password | enable password for ASA zero day config | `string` | n/a | yes |
| fingerprint | n/a | `any` | n/a | yes |
| inside\_network | inside network name | `string` | `""` | no |
| label\_prefix | a string that will be prepended to all resources | `string` | `"none"` | no |
| mgmt\_network | management network name | `string` | `""` | no |
| networks | a list of VPC | `list(object({ name = string, vcn_cidr = string, subnet_cidr = string, private_ip = list(string), external_ip = bool }))` | `[]` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| outside\_network | outside network name | `string` | `""` | no |
| private\_key\_path | n/a | `any` | n/a | yes |
| region | The region | `any` | n/a | yes |
| tenancy\_ocid | n/a | `any` | n/a | yes |
| user\_ocid | n/a | `any` | n/a | yes |
| vm\_ads\_number | The Availability Domain Number for vm, OCI Availability Domains: 1,2,3  (subject to region availability) | `list(number)` | <pre>[<br>  1<br>]</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| networks\_list | list of networks |
| networks\_map | map of networks |
| vm\_external\_ips | external ips for created instances |
| vm\_private\_ips | Private IPs of created instances. |

<!--- END_TF_DOCS --->
