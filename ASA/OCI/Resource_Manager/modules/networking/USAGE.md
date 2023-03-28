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
| dmz1\_network | dmz1 network name | `string` | n/a | yes |
| dmz2\_network | dmz2 network name | `string` | n/a | yes |
| inside\_network | inside network name | `string` | n/a | yes |
| label\_prefix | a string that will be prepended to all resources | `string` | `"none"` | no |
| mgmt\_network | management network name | `string` | n/a | yes |
| networks | a list of VPC | `list(object({ name = string, vcn_cidr = string, subnet_cidr = string, private_ip = list(string), external_ip = bool }))` | `[]` | no |
| outside\_network | outside network name | `string` | n/a | yes |
| region | The region | `any` | n/a | yes |
| tags | simple key-value pairs to tag the resources created | `map(any)` | <pre>{<br>  "module": "oracle-terraform-modules/vcn/oci",<br>  "terraformed": "yes"<br>}</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| networks\_list | A list of network related info such as name, links,subnet links, cidr, internal IP, has external IP or not etc |
| networks\_map | A map of network related info such as name, links,subnet links, cir, internal IP, has external IP or not etc |

<!--- END_TF_DOCS --->
