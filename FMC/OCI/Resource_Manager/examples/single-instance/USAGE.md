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
| appliance\_ips | internal IP addresses for cisco appliance | `list(string)` | `[]` | no |
| compartment\_id | compartment id where to create all resources | `string` | n/a | yes |
| day\_0\_config | Render a startup script with a template. | `string` | `""` | no |
| fingerprint | n/a | `any` | n/a | yes |
| hostname | FMC hostname | `string` | `"fmc"` | no |
| label\_prefix | a string that will be prepended to all resources | `string` | `"none"` | no |
| mangement\_subnet\_cidr\_block | Management Subnet CIDR | `string` | `"10.22.0.0/24"` | no |
| mangement\_vcn\_cidr\_block | VCN CIDR | `string` | `"10.22.0.0/16"` | no |
| mangement\_vcn\_display\_name | management VCN Name | `string` | `"mgmt"` | no |
| multiple\_ad | n/a | `bool` | `false` | no |
| network\_strategy | n/a | `string` | `"Create New VCN and Subnet"` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| private\_key\_path | n/a | `any` | n/a | yes |
| region | The region | `any` | n/a | yes |
| subnet\_id | existing subnet id for managment network's subnet | `string` | `""` | no |
| tenancy\_ocid | ########################### Provider Configuration  # ########################### | `any` | n/a | yes |
| user\_ocid | n/a | `any` | n/a | yes |
| vm\_compute\_shape | Compute Shape | `string` | `"VM.Standard2.4"` | no |

## Outputs

| Name | Description |
|------|-------------|
| subnet\_id | subnet\_id |
| vm\_external\_ips | external ips for created instances |
| vm\_private\_ips | Private IPs of created instances. |

<!--- END_TF_DOCS --->
