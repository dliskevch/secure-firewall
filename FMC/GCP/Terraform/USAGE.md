# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| terraform | >=1.0.0 |
| google | <4.0,>= 3.79 |
| google-beta | <4.0,>= 3.79 |
| random | >= 3.1.0 |
| template | >= 2.2.0 |

## Providers

| Name | Version |
|------|---------|
| google | <4.0,>= 3.79 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| admin\_password | password for fmc admin | `string` | n/a | yes |
| admin\_ssh\_pub\_key | ssh public key for admin | `string` | n/a | yes |
| appliance\_ips | internal IP addresses for cisco appliance | `list(string)` | `[]` | no |
| boot\_disk\_size | Root disk size in GB | `string` | `"250"` | no |
| boot\_disk\_type | The GCE boot disk type.Set to pd-standard (for PD HDD). | `string` | `"pd-ssd"` | no |
| cisco\_product\_version | cisco product version | `string` | `"cisco-fmcv-7-0-0-94"` | no |
| custom\_route\_tag | tag for custom route | `string` | `"cisco-fmc"` | no |
| day\_0\_config | Render a startup script with a template. | `string` | `""` | no |
| hostname | FMCv OS hostname | `string` | `"fmc"` | no |
| network | The name of the VPC network for Vault. | `string` | `""` | no |
| network\_project\_id | The project ID of the shared VPC's host (for shared vpc support) | `string` | `""` | no |
| network\_subnet\_cidr\_range | CIDR block range for the subnet. | `string` | `"10.127.0.0/24"` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| project\_id | The project ID to host the network in | `string` | n/a | yes |
| project\_services | List of services to enable on the project where Vault will run. These services are required in order for this Vault setup to function. | `list(string)` | <pre>[<br>  "compute.googleapis.com",<br>  "iam.googleapis.com"<br>]</pre> | no |
| region | The region | `string` | n/a | yes |
| subnet | The name of the VPC subnetwork for Vault. By default, one will be created for you. | `string` | `""` | no |
| vm\_instance\_labels | Labels to apply to the vm instances. | `map(string)` | `{}` | no |
| vm\_instance\_tags | Additional tags to apply to the instances, please note the service account is used as much as possible as best practice | `list(string)` | `[]` | no |
| vm\_machine\_type | machine type for appliance | `string` | `"e2-standard-4"` | no |

## Outputs

| Name | Description |
|------|-------------|
| subnet\_name | subnet name |
| vm\_external\_ips | external ips for vm |

<!--- END_TF_DOCS --->
