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
| appliance\_ips | internal IP addresses for cisco appliance | `list(string)` | `[]` | no |
| compartment\_id | compartment id where to create all resources | `string` | n/a | yes |
| label\_prefix | a string that will be prepended to all resources | `string` | `"none"` | no |
| mangement\_subnet\_cidr\_block | Management Subnet CIDR | `string` | `"10.22.0.0/24"` | no |
| mangement\_vcn\_cidr\_block | VCN CIDR | `string` | `"10.22.0.0/16"` | no |
| mangement\_vcn\_display\_name | management VCN Name | `string` | `"mgmt"` | no |
| region | The region | `any` | n/a | yes |
| tags | simple key-value pairs to tag the resources created | `map(any)` | <pre>{<br>  "module": "oracle-terraform-modules/vcn/oci",<br>  "terraformed": "yes"<br>}</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| subnet\_id | subnet id |

<!--- END_TF_DOCS --->
