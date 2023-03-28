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
| availability\_zone\_count | n/a | `number` | `1` | no |
| aws\_access\_key | n/a | `any` | n/a | yes |
| aws\_secret\_key | n/a | `any` | n/a | yes |
| create\_fmc | Boolean value to create FMC or not | `bool` | `true` | no |
| create\_igw | n/a | `bool` | `false` | no |
| diag\_interface\_id | n/a | `list(string)` | `[]` | no |
| diag\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| diag\_subnet\_name | n/a | `list(string)` | `[]` | no |
| fmc\_ip | n/a | `string` | `""` | no |
| ftd\_diag\_ip | n/a | `list` | `[]` | no |
| ftd\_inside\_ip | n/a | `list` | `[]` | no |
| ftd\_mgmt\_ip | n/a | `list` | `[]` | no |
| ftd\_outside\_ip | n/a | `list` | `[]` | no |
| ftd\_size | n/a | `string` | `"c5.xlarge"` | no |
| inside\_interface\_sg | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| inside\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| inside\_subnet\_name | n/a | `list(string)` | `[]` | no |
| instances\_per\_az | n/a | `number` | `1` | no |
| keyname | n/a | `any` | n/a | yes |
| mgmt\_interface\_id | n/a | `list(string)` | `[]` | no |
| mgmt\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| mgmt\_subnet\_name | n/a | `list(string)` | `[]` | no |
| outside\_interface\_id | n/a | `list(string)` | `[]` | no |
| outside\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| outside\_subnet\_name | n/a | `list(string)` | `[]` | no |
| region | n/a | `string` | `"us-east-1"` | no |
| security\_group\_egress | Can be specified multiple times for each egress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>    description = string<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "10.0.0.0/8"<br>    ],<br>    "description": null,<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| security\_group\_ingress\_with\_cidr | Can be specified multiple times for each ingress rule. | <pre>list(object({<br>    from_port   = number<br>    protocol    = string<br>    to_port     = number<br>    cidr_blocks = list(string)<br>    description = string<br>  }))</pre> | <pre>[<br>  {<br>    "cidr_blocks": [<br>      "0.0.0.0/0"<br>    ],<br>    "description": null,<br>    "from_port": 0,<br>    "protocol": "-1",<br>    "to_port": 0<br>  }<br>]</pre> | no |
| tags | n/a | `map(any)` | `{}` | no |
| vpc\_cidr | n/a | `any` | `null` | no |
| vpc\_name | n/a | `string` | `null` | no |

## Outputs

| Name | Description |
|------|-------------|
| instance\_ip | Public IP address of the EC2 instance |
| service\_mgmt\_subnets | n/a |

<!--- END_TF_DOCS --->
