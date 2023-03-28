# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| aws | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| GWLBE\_Subnet\_Routetable\_IDs | list of Route table IDs associated with GWLBE Subnets | `list(string)` | `[]` | no |
| NAT\_Subnet\_Routetable\_IDs | list of Route table IDs associated with NAT Subnets | `list(string)` | `[]` | no |
| availability\_zone\_count | n/a | `number` | `2` | no |
| aws\_availability\_zones | n/a | `number` | `2` | no |
| gwlbe | ID of the GWLB Endpoints | `list(string)` | n/a | yes |
| service\_subnet\_cidr | CIDRs of the service TGW Subnet | `list(string)` | `[]` | no |
| spoke\_rt\_id | n/a | `any` | n/a | yes |
| spoke\_subnet\_cidr | CIDRs for new spoke TGW subnets | `list(string)` | `[]` | no |
| spoke\_subnet\_id | n/a | `any` | n/a | yes |
| tgw\_subnet\_cidr | n/a | `any` | n/a | yes |
| tgw\_subnet\_name | n/a | `any` | n/a | yes |
| transit\_gateway\_name | Name of the Transit Gateway created | `string` | `null` | no |
| vpc\_service\_id | n/a | `any` | n/a | yes |
| vpc\_spoke\_cidr | n/a | `any` | n/a | yes |
| vpc\_spoke\_id | n/a | `any` | n/a | yes |

## Outputs

No output.

<!--- END_TF_DOCS --->
