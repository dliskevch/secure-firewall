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
| custom\_route\_tag | tag for custom route | `string` | n/a | yes |
| diag\_network | diag network name | `string` | n/a | yes |
| dmz\_network | dmz network name | `string` | n/a | yes |
| inside\_network | inside network name | `string` | n/a | yes |
| mgmt\_network | management network name | `string` | n/a | yes |
| networks | a list of VPC | `list(object({ name = string, cidr = string, appliance_ip = list(string), external_ip = bool }))` | `[]` | no |
| outside\_network | outside network name | `string` | n/a | yes |
| project\_id | The project ID to host the network in | `any` | n/a | yes |
| region | The region | `any` | n/a | yes |
| service\_account | The email address of the service account which will be assigned to the compute instances. | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| networks\_list | A list of network related info such as name, links,subnet links, cir, internal IP, has external IP or not etc |

<!--- END_TF_DOCS --->
