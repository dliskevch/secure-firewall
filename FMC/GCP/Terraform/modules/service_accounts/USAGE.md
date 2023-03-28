# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| google | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| sa\_account\_id | service account id | `string` | `""` | no |
| sa\_description | Default description of the created service accounts (defaults to no description) | `string` | `""` | no |
| sa\_display\_name | Display names of the created service accounts (defaults to 'Terraform-managed service account') | `string` | `"Terraform-managed service account"` | no |

## Outputs

| Name | Description |
|------|-------------|
| email | The email address of the service account. |

<!--- END_TF_DOCS --->
