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
| appliance\_ips | internal IP addresses for cisco appliance | `list(string)` | `[]` | no |
| compartment\_id | compartment id where to create all resources | `string` | n/a | yes |
| day\_0\_config | zero day configuration | `string` | `""` | no |
| hostname | FMC hostname | `string` | `"fmc"` | no |
| mp\_listing\_resource\_id | Marketplace Listing Image OCID | `string` | `""` | no |
| multiple\_ad | n/a | `bool` | `false` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| region | The region | `string` | n/a | yes |
| subnet\_id | existing subnet id for managment network's subnet | `string` | `""` | no |
| tenancy\_ocid | n/a | `any` | n/a | yes |
| vm\_compute\_shape | Compute Shape | `string` | `"VM.Standard2.4"` | no |

## Outputs

| Name | Description |
|------|-------------|
| external\_ips | external ips for VPC networks |
| instance\_ids | ocid of created instances. |
| private\_ips | Private IPs of created instances. |

<!--- END_TF_DOCS --->
