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
| asa01\_dmz\_ip | n/a | `string` | `"10.0.4.10"` | no |
| asa01\_inside\_ip | n/a | `string` | `"10.0.3.10"` | no |
| asa01\_mgmt\_ip | n/a | `string` | `"10.0.1.10"` | no |
| asa01\_outside\_ip | n/a | `string` | `"10.0.5.10"` | no |
| asa02\_dmz\_ip | n/a | `string` | `"10.0.40.20"` | no |
| asa02\_inside\_ip | n/a | `string` | `"10.0.30.20"` | no |
| asa02\_mgmt\_ip | n/a | `string` | `"10.0.10.20"` | no |
| asa02\_outside\_ip | n/a | `string` | `"10.0.50.20"` | no |
| asa\_size | n/a | `string` | `"c5.2xlarge"` | no |
| availability\_zone\_count | n/a | `number` | `2` | no |
| aws\_access\_key | n/a | `any` | n/a | yes |
| aws\_secret\_key | n/a | `any` | n/a | yes |
| dmz01\_subnet | n/a | `string` | `"10.0.4.0/24"` | no |
| dmz02\_subnet | n/a | `string` | `"10.0.40.0/24"` | no |
| health\_check | n/a | `map` | <pre>{<br>  "port": 22,<br>  "protocol": "TCP"<br>}</pre> | no |
| inside01\_subnet | n/a | `string` | `"10.0.3.0/24"` | no |
| inside02\_subnet | n/a | `string` | `"10.0.30.0/24"` | no |
| instances\_per\_az | n/a | `number` | `2` | no |
| key\_name | n/a | `any` | n/a | yes |
| keyname | Existing SSH Key on the AWS | `string` | `"NGFW-KP"` | no |
| listener\_ports | n/a | `map` | <pre>{<br>  "22": "TCP"<br>}</pre> | no |
| mgmt01\_subnet | n/a | `string` | `"10.0.1.0/24"` | no |
| mgmt02\_subnet | n/a | `string` | `"10.0.10.0/24"` | no |
| outside01\_subnet | n/a | `string` | `"10.0.5.0/24"` | no |
| outside02\_subnet | n/a | `string` | `"10.0.50.0/24"` | no |
| region | n/a | `string` | `"us-east-1"` | no |
| vpc\_cidr | defining the VPC CIDR | `string` | `"10.0.0.0/16"` | no |
| vpc\_name | n/a | `string` | `"Service-VPC"` | no |

## Outputs

| Name | Description |
|------|-------------|
| asa01ip | ################################################################################################################################# Output ################################################################################################################################# |
| asa02ip | n/a |

<!--- END_TF_DOCS --->
