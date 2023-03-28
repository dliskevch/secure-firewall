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
| availability\_zone\_count | n/a | `number` | `2` | no |
| create\_igw | n/a | `bool` | `false` | no |
| diag\_interface | n/a | `list(string)` | `[]` | no |
| diag\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| diag\_subnet\_name | n/a | `list(string)` | <pre>[<br>  "diag1",<br>  "diag2"<br>]</pre> | no |
| fmc\_interface | n/a | `string` | `""` | no |
| fmc\_ip | n/a | `string` | `""` | no |
| fmc\_mgmt\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| ftd\_diag\_ip | n/a | `list` | `[]` | no |
| ftd\_inside\_ip | n/a | `list` | `[]` | no |
| ftd\_mgmt\_ip | n/a | `list` | `[]` | no |
| ftd\_outside\_ip | n/a | `list` | `[]` | no |
| inside\_interface | n/a | `list(string)` | `[]` | no |
| inside\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| inside\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| inside\_subnet\_name | n/a | `list(string)` | <pre>[<br>  "inside1",<br>  "inside2"<br>]</pre> | no |
| instances\_per\_az | n/a | `number` | `1` | no |
| mgmt\_interface | n/a | `list(string)` | `[]` | no |
| mgmt\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| mgmt\_subnet\_cidr | if subnet cidr empty then use existing based on subnet name | `list(string)` | `[]` | no |
| mgmt\_subnet\_name | provide default values for subnet name as it is used in both cases | `list(string)` | <pre>[<br>  "mgmt1",<br>  "mgmt2"<br>]</pre> | no |
| outside\_interface | n/a | `list(string)` | `[]` | no |
| outside\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| outside\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| outside\_subnet\_name | n/a | `list(string)` | <pre>[<br>  "outside1",<br>  "outside2"<br>]</pre> | no |
| tags | n/a | `map(any)` | `{}` | no |
| vpc\_cidr | if vpc\_cidr empty then use existing | `string` | `""` | no |
| vpc\_name | n/a | `string` | `"IAC-VPC"` | no |

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
| mgmt\_sub | n/a |
| mgmt\_subnet | n/a |
| outside\_interface | n/a |
| outside\_interface\_ip | n/a |
| outside\_subnet | n/a |
| vpc\_id | n/a |

<!--- END_TF_DOCS --->
