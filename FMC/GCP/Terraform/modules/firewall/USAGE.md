# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| terraform | >=1.0.3 |
| google | <4.0,>= 3.77 |

## Providers

| Name | Version |
|------|---------|
| google | <4.0,>= 3.77 |
| random | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| network | The name of the VPC network for Vault. | `string` | `""` | no |
| project\_id | The project ID to host the network in | `any` | n/a | yes |
| service\_account | The email address of the service account which will be assigned to the compute instances. | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| https\_firewall\_rule | The created https firewall rule resources |
| ssh\_firewall\_rule | The created ssh firewall rule resources |

<!--- END_TF_DOCS --->
