# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

No provider.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| appliance\_ips | internal IP addresses for cisco appliance | `list(string)` | `[]` | no |
| custom\_route\_tag | tag for custom route | `string` | n/a | yes |
| network | The name of the VPC network for Vault. | `string` | `""` | no |
| network\_subnet\_cidr\_range | CIDR block range for the subnet. | `string` | `"10.127.0.0/24"` | no |
| project\_id | The project ID to host the network in | `any` | n/a | yes |
| region | The region | `any` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| subnet\_name | subnet self link of management network |
| subnet\_self\_link | subnet self link of management network |

<!--- END_TF_DOCS --->
