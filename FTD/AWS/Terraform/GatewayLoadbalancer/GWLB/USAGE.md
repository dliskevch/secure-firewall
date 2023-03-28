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
| GWLB\_name | name for Gateway loadbalancer | `string` | `"GWLB"` | no |
| appliance\_subnet | list of subnets for GWLB | `list(string)` | `[]` | no |
| aws\_access\_key | AWS access key id | `string` | n/a | yes |
| aws\_availability\_zones | list of availability\_zones | `list(string)` | <pre>[<br>  "us-east-1f",<br>  "us-east-1a"<br>]</pre> | no |
| aws\_secret\_key | AWS secret key id | `string` | n/a | yes |
| igw\_name | Name of the Internet Gateway attached to Existing VPC | `string` | `""` | no |
| instance | list of instance ip address that will be attached to target group of GWLB | `list(string)` | `[]` | no |
| region | AWS region | `string` | n/a | yes |
| use\_existing\_vpc | Setting to determine if GWLB needs to be created in a new or existing VPC | `bool` | n/a | yes |
| vpc\_cidr | VPC cidr block for new VPC | `string` | `"172.16.0.0/16"` | no |
| vpc\_name | name for VPC | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| az-id\_endpoint\_map | n/a |
| gwlbe\_route\_table | n/a |
| nat\_route\_table | n/a |
| vpc\_id | n/a |

<!--- END_TF_DOCS --->
