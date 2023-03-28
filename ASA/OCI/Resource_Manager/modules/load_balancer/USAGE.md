# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| oci | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| compartment\_id | compartment id where to create all resources | `string` | n/a | yes |
| inside\_network | inside network name | `string` | `""` | no |
| instance\_ids | ocid of vm instances | `list(string)` | n/a | yes |
| multiple\_ad | n/a | `bool` | `false` | no |
| networks\_map | networks in a map(network\_name) | `map(object({ name = string, vcn_id = string, subnet_id = string, subnet_cidr = string, private_ip = list(string), external_ip = bool }))` | n/a | yes |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| outside\_network | management network name | `string` | `""` | no |
| region | The region | `string` | n/a | yes |
| service\_port | service port | `number` | n/a | yes |
| tenancy\_ocid | n/a | `any` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| external\_lb\_ip | The external ip address of the public LB |
| internal\_lb\_ip | The internal ip address of the private LB |

<!--- END_TF_DOCS --->
