# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| terraform | >=1.0.0 |
| google | ~> 3.80, <4.0 |
| google-beta | ~> 3.80, <4.0 |
| template | ~> 2.2.0 |

## Providers

| Name | Version |
|------|---------|
| google | ~> 3.80, <4.0 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| admin\_ssh\_pub\_key | ssh public key for admin | `string` | n/a | yes |
| allow\_global\_access | Internal LB allow global access or not | `bool` | `false` | no |
| cisco\_product\_version | cisco product version | `string` | `"cisco-asav-9-16-1-28"` | no |
| compute\_image | vm image | `string` | `""` | no |
| custom\_route\_tag | tag for custom route | `string` | `"cisco-asav"` | no |
| day\_0\_config | Render a startup script with a template. | `string` | `""` | no |
| dmz1\_network | dmz1 network name | `string` | `""` | no |
| dmz2\_network | dmz2 network name | `string` | `""` | no |
| enable\_password | enable password for ASA zero day config | `string` | n/a | yes |
| inside\_network | inside network name | `string` | `"vpc-inside"` | no |
| mgmt\_network | management network name | `string` | `""` | no |
| named\_ports | Named name and port. https://cloud.google.com/load-balancing/docs/backend-service#named_ports | <pre>list(object({<br>    name = string<br>    port = number<br>  }))</pre> | <pre>[<br>  {<br>    "name": "console",<br>    "port": 22<br>  },<br>  {<br>    "name": "https",<br>    "port": 443<br>  }<br>]</pre> | no |
| networks | a list of VPC network info | `list(object({ name = string, cidr = string, appliance_ip = list(string), external_ip = bool }))` | `[]` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| outside\_network | outside network name | `string` | `""` | no |
| project\_id | The project ID to host the network in | `string` | n/a | yes |
| project\_services | List of services to enable on the project where Vault will run. These services are required in order for this Vault setup to function. | `list(string)` | <pre>[<br>  "compute.googleapis.com",<br>  "iam.googleapis.com"<br>]</pre> | no |
| region | The region | `string` | n/a | yes |
| service\_port | service port | `number` | `80` | no |
| startup\_script | vm image | `string` | `""` | no |
| use\_internal\_lb | use internal LB or not | `bool` | `false` | no |
| vm\_instance\_labels | Labels to apply to the vm instances. | `map(string)` | `{}` | no |
| vm\_instance\_tags | Additional tags to apply to the instances, please note the service account is used as much as possible as best practice | `list(string)` | `[]` | no |
| vm\_machine\_type | machine type for appliance | `string` | `"e2-standard-4"` | no |
| vm\_zones | The zones of vm instances | `list(string)` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| external\_lb\_ip | The external ip address of the load balancer |
| internal\_lb\_ip | The internal ip address of the load balancer |
| networks\_map | map of networks |
| vm\_external\_ips | external ips for vm |

<!--- END_TF_DOCS --->
