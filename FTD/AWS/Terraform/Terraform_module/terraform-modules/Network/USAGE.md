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
| availability\_zone\_count | Spacified availablity zone count . | `number` | `2` | no |
| create\_igw | Condition to create IGW . | `bool` | `false` | no |
| diag\_interface | list out Diagonstic interface . | `list(string)` | `[]` | no |
| diag\_subnet\_cidr | List out diagonastic Subnet CIDR . | `list(string)` | `[]` | no |
| diag\_subnet\_name | Spacified diagonstic subnet name . | `list(string)` | `[]` | no |
| fmc\_interface | Spacified FMCv interface . | `string` | `""` | no |
| fmc\_ip | List out FMCv IPs . | `string` | `""` | no |
| fmc\_mgmt\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| ftd\_diag\_ip | List out FTD Diagonostic IPs . | `list` | `[]` | no |
| ftd\_inside\_ip | List FTD inside IPs . | `list(string)` | `[]` | no |
| ftd\_mgmt\_ip | List out management IPs . | `list(string)` | `[]` | no |
| ftd\_outside\_ip | List outside IPs . | `list` | `[]` | no |
| inside\_interface | list out Inside interface . | `list(string)` | `[]` | no |
| inside\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| inside\_subnet\_cidr | List out inside Subnet CIDR . | `list(string)` | `[]` | no |
| inside\_subnet\_name | Spacified inside subnet name . | `list(string)` | `[]` | no |
| instances\_per\_az | Spacified no. of instance per az wants to be create . | `number` | `1` | no |
| mgmt\_interface | list out management interface . | `list(string)` | `[]` | no |
| mgmt\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| mgmt\_subnet\_cidr | List out management Subnet CIDR . | `list(string)` | `[]` | no |
| mgmt\_subnet\_name | Spacified management subnet name . | `list(string)` | `[]` | no |
| outside\_interface | list out outside interface . | `list(string)` | `[]` | no |
| outside\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| outside\_subnet\_cidr | List out outside Subnet CIDR . | `list(string)` | `[]` | no |
| outside\_subnet\_name | Spacified outside subnet name . | `list(string)` | `[]` | no |
| tags | tags to map with resources . | `map(any)` | `{}` | no |
| use\_fmc\_eip | boolean value to use EIP on FMC or not | `bool` | `false` | no |
| use\_ftd\_eip | boolean value to use EIP on FTD or not | `bool` | `false` | no |
| vpc\_cidr | Specified CIDR for VPC . | `string` | `""` | no |
| vpc\_name | Specified VPC Name . | `string` | `"IAC-VPC"` | no |

## Outputs

| Name | Description |
|------|-------------|
| diag\_interface | n/a |
| diag\_interface\_ip | n/a |
| diag\_subnet | n/a |
| fmc\_interface\_ip | n/a |
| fmcmgmt\_interface | n/a |
| inside\_interface | n/a |
| inside\_interface\_ip | n/a |
| inside\_subnet | n/a |
| internet\_gateway | n/a |
| mgmt\_interface | n/a |
| mgmt\_interface\_ip | n/a |
| mgmt\_rt\_id | n/a |
| mgmt\_sub | n/a |
| mgmt\_subnet | n/a |
| outside\_interface | n/a |
| outside\_interface\_ip | n/a |
| outside\_subnet | n/a |
| vpc\_id | n/a |

<!--- END_TF_DOCS --->
