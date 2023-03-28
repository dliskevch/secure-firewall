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
| ASA\_version | n/a | `string` | `"asav9-15-1"` | no |
| asa\_dmz\_ip | n/a | `string` | `"10.1.4.10"` | no |
| asa\_inside\_ip | n/a | `string` | `"10.1.3.10"` | no |
| asa\_mgmt\_ip | n/a | `string` | `"10.1.0.10"` | no |
| asa\_outside\_ip | n/a | `string` | `"10.1.5.10"` | no |
| availability\_zone\_count | n/a | `number` | `1` | no |
| aws\_access\_key | n/a | `any` | n/a | yes |
| aws\_secret\_key | n/a | `any` | n/a | yes |
| dmz\_subnet | n/a | `string` | `"10.1.4.0/24"` | no |
| enable\_password | n/a | `string` | `"P@ssw0rd!"` | no |
| inside\_subnet | n/a | `string` | `"10.1.3.0/24"` | no |
| instances\_per\_az | n/a | `number` | `1` | no |
| key\_name | n/a | `any` | n/a | yes |
| keyname | Existing SSH Key on the AWS | `string` | `"NGFW-KP"` | no |
| mgmt\_subnet | n/a | `string` | `"10.1.0.0/24"` | no |
| outside\_subnet | n/a | `string` | `"10.1.5.0/24"` | no |
| region | n/a | `string` | `"us-east-1"` | no |
| size | n/a | `string` | `"c5.xlarge"` | no |
| vpc\_cidr | defining the VPC CIDR | `string` | `"10.1.0.0/16"` | no |
| vpc\_name | n/a | `string` | `"Service-VPC"` | no |

## Outputs

| Name | Description |
|------|-------------|
| ip | ################################################################################################################################# Output ################################################################################################################################# |

<!--- END_TF_DOCS --->
