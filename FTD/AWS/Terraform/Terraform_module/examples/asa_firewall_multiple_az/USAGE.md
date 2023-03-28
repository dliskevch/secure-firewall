# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.13.5 |
| aws | >= 2.7.0 |

## Providers

No provider.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| FMC\_version | specified FMC version. | `string` | `"fmcv-7.1.0"` | no |
| FTD\_version | specified FTD version. | `string` | `"ftdv-7.1.0"` | no |
| availability\_zone\_count | Spacified availablity zone count . | `number` | `2` | no |
| aws\_access\_key | n/a | `any` | n/a | yes |
| aws\_secret\_key | n/a | `any` | n/a | yes |
| create\_fmc | Boolean value to create FMC or not | `Bool` | `true` | no |
| create\_igw | n/a | `string` | `true` | no |
| diag\_interface\_id | n/a | `list(string)` | `[]` | no |
| diag\_subnet\_cidr | List out diagonastic Subnet CIDR . | `list(string)` | `[]` | no |
| diag\_subnet\_name | n/a | `list(string)` | `[]` | no |
| fmc\_admin\_password | spacified fmc admin password . | `string` | `"Cisco@123"` | no |
| fmc\_hostname | spacified fmc hostname . | `string` | `"FMC-01"` | no |
| fmc\_interface\_id | Spacified FMCv interface . | `string` | `""` | no |
| fmc\_ip | List out FMCv IPs . | `string` | `""` | no |
| fmc\_mgmt\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| ftd\_diag\_ip | List out FTD Diagonostic IPs . | `list` | `[]` | no |
| ftd\_inside\_ip | n/a | `list` | `[]` | no |
| ftd\_mgmt\_ip | n/a | `list` | `[]` | no |
| ftd\_outside\_ip | n/a | `list` | `[]` | no |
| ftd\_size | specified server instance type . | `string` | `"c5.4xlarge"` | no |
| inside\_interface\_id | n/a | `list(string)` | `[]` | no |
| inside\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| inside\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| inside\_subnet\_name | n/a | `list(string)` | `[]` | no |
| instances\_per\_az | Spacified no. of instance per az wants to be create . | `number` | `1` | no |
| keyname | specified key pair name to connect firewall . | `string` | n/a | yes |
| mgmt\_interface\_id | n/a | `list(string)` | `[]` | no |
| mgmt\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| mgmt\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| mgmt\_subnet\_name | n/a | `list(string)` | `[]` | no |
| outside\_interface\_id | n/a | `list(string)` | `[]` | no |
| outside\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| outside\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| outside\_subnet\_name | n/a | `list(string)` | `[]` | no |
| reg\_key | spacified reg key . | `string` | `"cisco"` | no |
| region | n/a | `string` | `"us-east-1"` | no |
| tags | n/a | `map(any)` | `{}` | no |
| use\_fmc\_eip | boolean value to use EIP on FMC or not | `bool` | `false` | no |
| use\_ftd\_eip | boolean value to use EIP on FTD or not | `bool` | `false` | no |
| vpc\_cidr | n/a | `any` | `null` | no |
| vpc\_name | n/a | `string` | `null` | no |

## Outputs

No output.

<!--- END_TF_DOCS --->
