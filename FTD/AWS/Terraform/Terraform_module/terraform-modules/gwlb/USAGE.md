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
| GWLB\_name | name for Gateway loadbalancer | `string` | n/a | yes |
| availability\_zone\_count | n/a | `number` | `2` | no |
| gwlb\_subnet | GWLB subnet | `string` | n/a | yes |
| gwlb\_vpc\_id | GWLB vpc id | `string` | n/a | yes |
| instance\_ip | list of instance ip address that will be attached to target group of GWLB | `list(string)` | `[]` | no |

## Outputs

| Name | Description |
|------|-------------|
| gwlb | n/a |

<!--- END_TF_DOCS --->
