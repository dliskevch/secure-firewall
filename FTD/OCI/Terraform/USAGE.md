# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

| Name | Version |
|------|---------|
| terraform | >=1.0.0 |
| oci | ~> 4.46.0 |
| template | ~> 2.2.0 |

## Providers

No provider.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| admin\_password | password for admin | `string` | n/a | yes |
| admin\_ssh\_pub\_key | ssh public key for admin | `string` | n/a | yes |
| compartment\_id | compartment id where to create all resources | `string` | n/a | yes |
| day\_0\_config | Render a startup script with a template. | `string` | `"startup_file.json"` | no |
| diag\_network | diag network name | `string` | `""` | no |
| dmz\_network | dmz network name | `string` | `""` | no |
| fingerprint | n/a | `any` | n/a | yes |
| hostname | FTD hostname | `string` | `"ftd"` | no |
| inside\_network | inside network name | `string` | `"vpc-inside"` | no |
| label\_prefix | a string that will be prepended to all resources | `string` | `"none"` | no |
| mgmt\_network | management network name | `string` | `""` | no |
| mp\_listing\_resource\_id | Marketplace Listing Image OCID | `string` | `"ocid1.image.oc1..aaaaaaaamybyw5im3tfl5fimi3nd57no3mtczwenrll7fgkzi4zgbc32tlqa"` | no |
| networks | a list of VPC network info | `list(object({ name = string, vcn_cidr = string, subnet_cidr = string, private_ip = list(string), external_ip = bool }))` | `[]` | no |
| num\_instances | Number of instances to create. This value is ignored if static\_ips is provided. | `number` | `1` | no |
| outside\_network | outside network name | `string` | `""` | no |
| private\_key | The contents of the private key file. Required if private\_key\_path is not defined, and takes precedence over private\_key\_path if both are defined. | `any` | n/a | yes |
| private\_key\_path | n/a | `any` | n/a | yes |
| region | the OCI region where resources will be created | `string` | `null` | no |
| tenancy\_ocid | ########################### Provider Configuration  # ########################### | `any` | n/a | yes |
| user\_ocid | n/a | `any` | n/a | yes |
| vm\_ads\_number | The Availability Domain Number for vm, OCI Availability Domains: 1,2,3  (subject to region availability) | `list(number)` | <pre>[<br>  1<br>]</pre> | no |
| vm\_compute\_shape | Compute Shape | `string` | `"VM.Standard2.4"` | no |

## Outputs

| Name | Description |
|------|-------------|
| networks\_list | A list of network related info such as name, links,subnet links, cidr, internal IP, has external IP or not etc |
| vm\_external\_ips | external ips for created instances. |
| vm\_private\_ips | Private IPs of created instances. |

<!--- END_TF_DOCS --->
