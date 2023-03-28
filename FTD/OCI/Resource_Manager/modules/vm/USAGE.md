# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| oci | n/a |
| random | n/a |
| template | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| admin\_password | enable password for zero day config | `string` | n/a | yes |
| admin\_ssh\_pub\_key | ssh public key for admin | `string` | n/a | yes |
| compartment\_id | compartment id where to create all resources | `string` | n/a | yes |
| day\_0\_config | zero day configuration | `string` | `""` | no |
| hostname | FTD hostname | `string` | `"ftd"` | no |
| mp\_listing\_resource\_id | Marketplace Listing Image OCID | `string` | `"ocid1.image.oc1..aaaaaaaamybyw5im3tfl5fimi3nd57no3mtczwenrll7fgkzi4zgbc32tlqa"` | no |
| multiple\_ad | n/a | `bool` | `false` | no |
| network\_5\_name | n/a | `any` | n/a | yes |
| networks\_list | network links in a map(network\_name) | `list(object({ name = string, vcn_id = string, subnet_id = string, subnet_cidr = string, private_ip = list(string), external_ip = bool }))` | n/a | yes |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| region | The region | `string` | n/a | yes |
| tenancy\_ocid | n/a | `any` | n/a | yes |
| vm\_compute\_shape | Compute Shape | `string` | `"VM.Standard2.4"` | no |

## Outputs

| Name | Description |
|------|-------------|
| external\_ips | external ips for VPC networks |
| instance\_ids | ocid of created instances. |
| private\_ips | Private IPs of created instances. |

<!--- END_TF_DOCS --->
