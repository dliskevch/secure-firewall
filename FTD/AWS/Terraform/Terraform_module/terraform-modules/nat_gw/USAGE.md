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
| ngw\_subnet\_cidr | Spacified ngw subnet CIDR   . | `list(string)` | `[]` | no |
| ngw\_subnet\_name | Spacified ngw subnet name . | `list(string)` | `[]` | no |
| vpc\_id | Specified VPC ID . | `string` | `""` | no |

## Outputs

| Name | Description |
|------|-------------|
| nat\_rt\_id | n/a |
| ngw | n/a |

<!--- END_TF_DOCS --->
