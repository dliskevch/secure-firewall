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
| FTD\_version | n/a | `string` | `"ftdv-6.7.0"` | no |
| aws\_access\_key | n/a | `any` | n/a | yes |
| aws\_az | Including the Avilability Zone | `string` | `"us-east-2a"` | no |
| aws\_secret\_key | n/a | `any` | n/a | yes |
| diag\_subnet | n/a | `string` | `"10.0.2.0/24"` | no |
| dmz\_subnet | n/a | `string` | `"10.0.4.0/24"` | no |
| ftd01\_diag\_ip | n/a | `string` | `"10.0.2.10"` | no |
| ftd01\_dmz\_ip | n/a | `string` | `"10.0.4.10"` | no |
| ftd01\_inside\_ip | n/a | `string` | `"10.0.3.10"` | no |
| ftd01\_mgmt\_ip | n/a | `string` | `"10.0.1.10"` | no |
| ftd01\_outside\_ip | n/a | `string` | `"10.0.5.10"` | no |
| inside\_subnet | n/a | `string` | `"10.0.3.0/24"` | no |
| key\_name | n/a | `any` | n/a | yes |
| keyname | Existing SSH Key on the AWS | `string` | `"NGFW-KP"` | no |
| mgmt\_subnet | n/a | `string` | `"10.0.1.0/24"` | no |
| outside\_subnet | n/a | `string` | `"10.0.5.0/24"` | no |
| region | n/a | `string` | `"us-east-2"` | no |
| size | n/a | `string` | `"c5.4xlarge"` | no |
| vpc\_cidr | defining the VPC CIDR | `string` | `"10.0.0.0/16"` | no |
| vpc\_name | n/a | `string` | `"Service-VPC"` | no |

## Outputs

| Name | Description |
|------|-------------|
| ip | ################################################################################################################################# Output ################################################################################################################################# |

<!--- END_TF_DOCS --->
