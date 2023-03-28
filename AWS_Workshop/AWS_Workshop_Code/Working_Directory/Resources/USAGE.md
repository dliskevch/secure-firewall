# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| aws | n/a |
| template | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| FMC\_version | n/a | `string` | `"fmcv-7.1.0"` | no |
| FTD\_version | n/a | `string` | `"ftdv-7.1.0"` | no |
| app\_interface | n/a | `list` | `[]` | no |
| app\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| app\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| app\_subnet\_name | n/a | `list(string)` | `[]` | no |
| availability\_zone\_count | n/a | `number` | `2` | no |
| aws\_access\_key | n/a | `any` | n/a | yes |
| aws\_secret\_key | n/a | `any` | n/a | yes |
| bastion\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| bastion\_ip | n/a | `string` | `""` | no |
| bastion\_subnet\_cidr | n/a | `string` | `""` | no |
| bastion\_subnet\_name | n/a | `string` | `""` | no |
| create | list the possible options as allowed values | `string` | `"both"` | no |
| create\_igw | n/a | `bool` | `false` | no |
| diag\_interface\_id | n/a | `list(string)` | `[]` | no |
| diag\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| diag\_subnet\_name | n/a | `list(string)` | `[]` | no |
| external\_health\_check | n/a | `map` | <pre>{<br>  "port": 22,<br>  "protocol": "TCP"<br>}</pre> | no |
| external\_listener\_ports | n/a | `list` | <pre>[<br>  {<br>    "port": 80,<br>    "protocol": "TCP",<br>    "target_type": "ip"<br>  }<br>]</pre> | no |
| fmc\_interface\_id | n/a | `string` | `""` | no |
| fmc\_ip | n/a | `string` | `""` | no |
| fmc\_mgmt\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| ftd\_app\_ip | n/a | `list` | `[]` | no |
| ftd\_diag\_ip | n/a | `list` | `[]` | no |
| ftd\_inside\_ip | n/a | `list` | `[]` | no |
| ftd\_mgmt\_ip | n/a | `list` | `[]` | no |
| ftd\_outside\_ip | n/a | `list` | `[]` | no |
| ftd\_size | n/a | `string` | `"c5.xlarge"` | no |
| inside\_interface\_id | n/a | `list(string)` | `[]` | no |
| inside\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| inside\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| inside\_subnet\_name | n/a | `list(string)` | `[]` | no |
| instances\_per\_az | n/a | `number` | `1` | no |
| internal\_health\_check | n/a | `map` | <pre>{<br>  "port": 22,<br>  "protocol": "TCP"<br>}</pre> | no |
| internal\_listener\_ports | n/a | `list` | <pre>[<br>  {<br>    "port": 80,<br>    "protocol": "TCP",<br>    "target_type": "ip"<br>  }<br>]</pre> | no |
| keyname | n/a | `string` | n/a | yes |
| mgmt\_interface\_id | n/a | `list(string)` | `[]` | no |
| mgmt\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| mgmt\_subnet\_cidr | if subnet cidr empty then use existing based on subnet name | `list(string)` | `[]` | no |
| mgmt\_subnet\_name | n/a | `list(string)` | `[]` | no |
| outside\_interface\_id | n/a | `list(string)` | `[]` | no |
| outside\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| outside\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| outside\_subnet\_name | n/a | `list(string)` | `[]` | no |
| region | n/a | `string` | `"us-east-1"` | no |
| tags | n/a | `map(any)` | `{}` | no |
| vpc\_cidr | n/a | `string` | `""` | no |
| vpc\_name | n/a | `string` | `"Transit-Service-VPC1"` | no |

## Outputs

| Name | Description |
|------|-------------|
| app\_interface | n/a |
| app\_interface\_ip | n/a |
| app\_subnet | n/a |

<!--- END_TF_DOCS --->
