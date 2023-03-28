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
| gwlb | n/a | `any` | n/a | yes |
| gwlbe\_subnet\_cidr | n/a | `list(string)` | `[]` | no |
| gwlbe\_subnet\_name | n/a | `list(string)` | `[]` | no |
| ngw\_id | n/a | `any` | n/a | yes |
| vpc\_id | n/a | `any` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| gwlb\_endpoint\_id | gwlb vpc endpoint |
| gwlbe\_rt\_id | n/a |

<!--- END_TF_DOCS --->
