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
| admin\_password | password for fmc admin | `string` | n/a | yes |
| admin\_ssh\_pub\_key | ssh public key for admin | `string` | n/a | yes |
| appliance\_ips | appliance IPs of management network | `list(string)` | n/a | yes |
| boot\_disk\_size | Root disk size in GB. | `any` | n/a | yes |
| boot\_disk\_type | The GCE boot disk type. May be set to pd-standard (for PD HDD) or pd-ssd. | `any` | n/a | yes |
| cisco\_product\_version | cisco product version | `string` | `"cisco-fmcv-7-0-0-94"` | no |
| day\_0\_config | zero day configuration | `string` | `""` | no |
| hostname | FMCv OS hostname | `string` | `"fmc"` | no |
| network\_project\_id | The project ID of the shared VPC's host (for shared vpc support) | `string` | `""` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| project\_id | The project ID to host the network in | `string` | n/a | yes |
| region | The region | `string` | n/a | yes |
| service\_account | The email address of the service account which will be assigned to the compute instances. | `string` | n/a | yes |
| subnet\_self\_link | subnet self link of management network | `any` | n/a | yes |
| vm\_instance\_labels | Labels to apply to the vm instances. | `map(string)` | `{}` | no |
| vm\_instance\_tags | Additional tags to apply to the instances, please note the service account is used as much as possible as best practice | `list(string)` | `[]` | no |
| vm\_machine\_type | machine type for appliance | `string` | `"e2-standard-4"` | no |

## Outputs

| Name | Description |
|------|-------------|
| external\_ips | external ips for VPC networks |

<!--- END_TF_DOCS --->
