# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| google | n/a |
| random | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| allow\_global\_access | Internal LB allow global access or not | `bool` | `false` | no |
| inside\_network | inside network name | `string` | `""` | no |
| instance\_ids | a list of google\_compute\_instance id | `list(string)` | `[]` | no |
| mgmt\_network | management network name | `string` | `""` | no |
| named\_ports | Named name and named port. https://cloud.google.com/load-balancing/docs/backend-service#named_ports | <pre>list(object({<br>    name = string<br>    port = number<br>  }))</pre> | `[]` | no |
| networks\_map | network links in a map(network\_name) | `map(object({ name = string, network_self_link = string, subnet_self_link = string, subnet_cidr = string, appliance_ip = list(string), external_ip = bool, routes = list(string) }))` | n/a | yes |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| project\_id | The project ID to host the network in | `string` | n/a | yes |
| region | The region | `string` | n/a | yes |
| service\_port | service port | `number` | n/a | yes |
| use\_internal\_lb | use internal LB or not | `bool` | `false` | no |
| vm\_zones | The zones | `list(string)` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| external\_ip\_ext\_fr | The external ip address of the forwarding rule. |
| internal\_ip\_ext\_fr | The  ip address of the forwarding rule. |

<!--- END_TF_DOCS --->
