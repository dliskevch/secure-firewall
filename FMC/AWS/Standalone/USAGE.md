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
| aws\_access\_key | n/a | `any` | n/a | yes |
| aws\_secret\_key | n/a | `any` | n/a | yes |
| azs | AWS Availability Zones | `list` | `[]` | no |
| fmc\_size | Size of the FMCv instance | `string` | `"c5.4xlarge"` | no |
| fmc\_version | Version of the FMCv | `string` | `"fmcv-7.0.0"` | no |
| hostname | FMCv OS hostname | `string` | `"fmc"` | no |
| igw\_id | Existing Internet Gateway ID | `string` | `""` | no |
| instances | Number of FMCv instances | `number` | `1` | no |
| key\_name | AWS EC2 Key | `any` | n/a | yes |
| name\_tag\_prefix | Prefix for the 'Name' tag of the resources | `string` | `"FMCv"` | no |
| password | Password for FMCv | `string` | `"P@$$w0rd1234"` | no |
| region | AWS Region | `any` | n/a | yes |
| subnet\_size | Size of Management subnet | `number` | `24` | no |
| subnets | mgmt subnets | `list` | `[]` | no |
| vpc\_cidr | VPC CIDR | `string` | `"10.0.0.0/16"` | no |
| vpc\_id | Existing VPC ID | `string` | `""` | no |
| vpc\_name | VPC Name | `string` | `"Cisco-FMCv"` | no |

## Outputs

| Name | Description |
|------|-------------|
| FMCv\_EIPs | n/a |

<!--- END_TF_DOCS --->
