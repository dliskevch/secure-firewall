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
| create | list the possible options as allowed values | `string` | `"both"` | no |
| external\_health\_check | n/a | `map` | <pre>{<br>  "port": 22,<br>  "protocol": "TCP"<br>}</pre> | no |
| external\_listener\_ports | n/a | `list` | <pre>[<br>  {<br>    "port": 80,<br>    "protocol": "TCP",<br>    "target_type": "ip"<br>  }<br>]</pre> | no |
| ftd\_inside\_ip | n/a | `list` | `[]` | no |
| ftd\_outside\_ip | n/a | `list` | `[]` | no |
| inside\_subnet\_id | n/a | `list` | `[]` | no |
| internal\_health\_check | n/a | `map` | <pre>{<br>  "port": 80,<br>  "protocol": "TCP"<br>}</pre> | no |
| internal\_listener\_ports | n/a | `list` | <pre>[<br>  {<br>    "port": 80,<br>    "protocol": "TCP",<br>    "target_type": "ip"<br>  }<br>]</pre> | no |
| outside\_subnet\_id | n/a | `list` | `[]` | no |
| vpc\_id | n/a | `any` | n/a | yes |

## Outputs

No output.

<!--- END_TF_DOCS --->
