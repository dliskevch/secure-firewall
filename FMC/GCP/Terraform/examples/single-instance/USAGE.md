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
| boot\_disk\_size | Root disk size in GB | `any` | n/a | yes |
| boot\_disk\_type | The GCE boot disk type.Set to pd-standard (for PD HDD). | `any` | n/a | yes |
| cisco\_product\_version | cisco product version | `string` | `"cisco-fmcv-7-0-0-94"` | no |
| day\_0\_config | Render a startup script with a template. | `string` | `""` | no |
| hostname | FMCv OS hostname | `string` | `"fmc"` | no |
| network | The name of the VPC network for Vault. | `string` | `""` | no |
| network\_subnet\_cidr\_range | CIDR block range for the subnet. | `string` | `"10.127.0.0/24"` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| project\_id | The project ID to host the network in | `any` | n/a | yes |
| region | The region | `any` | n/a | yes |
| subnet | The name of the VPC subnetwork for Vault. By default, one will be created for you. | `string` | `""` | no |
| vm\_instance\_labels | Labels to apply to the vm instances. | `map(string)` | `{}` | no |
| vm\_instance\_tags | Additional tags to apply to the instances, please note the service account is used as much as possible as best practice | `list(string)` | `[]` | no |
| vm\_machine\_type | machine type for appliance | `string` | `"e2-standard-4"` | no |

## Outputs

| Name | Description |
|------|-------------|
| subnet\_name | subnet name |
| vm\_external\_ips | external ips for VPC networks |

<!--- END_TF_DOCS --->
