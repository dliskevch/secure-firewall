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
| aws\_access\_key | AWS access key id | `string` | n/a | yes |
| aws\_availability\_zones | List of AZs to distribute service subnets | `list(string)` | <pre>[<br>  "ap-south-1a",<br>  "ap-south-1b"<br>]</pre> | no |
| aws\_secret\_key | AWS secret key id | `string` | n/a | yes |
| cidr\_service\_sub | CIDRs of the service TGW Subnet | `list(string)` | n/a | yes |
| cidr\_spoke\_sub | CIDRs for new spoke TGW subnets | `list(string)` | `[]` | no |
| gwlbe | ID of the GWLB Endpoints | `list(string)` | n/a | yes |
| id\_spoke\_sub | IDs for existing spoke subnets | `list(string)` | `[]` | no |
| region | AWS region | `string` | n/a | yes |
| subnet\_service\_name | Name of the service TGW subnet being created | `string` | `"Service-TGW-Subnet"` | no |
| subnet\_spoke\_name | Name of the spoke TGW subnet being created | `string` | `"Spoke-TGW-Subnet"` | no |
| transit\_gateway\_name | Name of the Transit Gateway created | `string` | `"TGW"` | no |
| vpc\_service\_id | VPC ID of Service VPC | `string` | n/a | yes |
| vpc\_spoke\_id | VPC ID of Spoke VPC | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| tgw\_id | n/a |

<!--- END_TF_DOCS --->
