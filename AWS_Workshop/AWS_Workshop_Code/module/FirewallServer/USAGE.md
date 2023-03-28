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
| FMC\_version | n/a | `string` | `"fmcv-7.1.0"` | no |
| FTD\_version | n/a | `string` | `"ftdv-7.1.0"` | no |
| availability\_zone\_count | n/a | `number` | `2` | no |
| fmc\_admin\_password | n/a | `string` | `"Cisco@123"` | no |
| fmc\_hostname | n/a | `string` | `"FMC-01"` | no |
| fmc\_mgmt\_ip | n/a | `string` | `""` | no |
| fmc\_nat\_id | n/a | `string` | `""` | no |
| fmcmgmt\_interface | n/a | `any` | n/a | yes |
| ftd\_diag\_interface | n/a | `any` | n/a | yes |
| ftd\_inside\_interface | n/a | `any` | n/a | yes |
| ftd\_mgmt\_interface | n/a | `any` | n/a | yes |
| ftd\_outside\_interface | n/a | `any` | n/a | yes |
| ftd\_size | n/a | `string` | `"c5.4xlarge"` | no |
| instances\_per\_az | n/a | `number` | `1` | no |
| keyname | n/a | `any` | n/a | yes |
| reg\_key | n/a | `string` | `"cisco"` | no |
| tags | n/a | `map` | `{}` | no |

## Outputs

No output.

<!--- END_TF_DOCS --->
