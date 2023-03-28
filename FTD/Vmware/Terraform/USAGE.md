# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| vsphere | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| cpu | FTDv number pf CPUs | `string` | `"4"` | no |
| datacenter | vSphere data center | `string` | n/a | yes |
| datastore | vSphere datastore | `string` | n/a | yes |
| dns1 | Primary DNS Server | `string` | `""` | no |
| dns2 | Secondary DNS Server | `string` | `""` | no |
| dns3 | Tertiary DNS Server | `string` | `""` | no |
| firewall\_mode | Firewall Mode | `string` | `"routed"` | no |
| fmc\_ip | Managing FMC IP | `string` | `""` | no |
| fmc\_nat\_id | FMC NAT ID | `string` | `""` | no |
| fmc\_regkey | FMC Registration key | `string` | `""` | no |
| host | vSphere host name | `string` | n/a | yes |
| hostname | FTDv hostname | `string` | n/a | yes |
| local\_manager | Enabled Manager locally | `string` | `"Yes"` | no |
| memory | FTDv memory allocation | `string` | `"8192"` | no |
| mgmt\_ip4 | Management IPv4 Address | `string` | `""` | no |
| mgmt\_ip4\_config | Management IPv4 Configuration | `string` | `"Manual"` | no |
| mgmt\_ip4\_gateway | Management IPv4 Gateway | `string` | `""` | no |
| mgmt\_ip4\_mask | Management IPv4 Mask | `string` | `""` | no |
| mgmt\_ip6 | Management IPv6 Address | `string` | `""` | no |
| mgmt\_ip6\_config | Management IPv6 Configuration | `string` | `"Disabled"` | no |
| mgmt\_ip6\_gateway | Management IPv6 Gateway | `string` | `""` | no |
| mgmt\_ip6\_mask | Management IPv6 Mask | `string` | `""` | no |
| network\_name1 | vSphere network name | `string` | n/a | yes |
| network\_name2 | vSphere network name | `string` | n/a | yes |
| network\_name3 | vSphere network name | `string` | n/a | yes |
| network\_name4 | vSphere network name | `string` | n/a | yes |
| password | Admin user password | `string` | n/a | yes |
| resource\_pool | vSphere resource\_pool name | `string` | n/a | yes |
| searchdomains | DNS Search Domains | `string` | `""` | no |
| vsphere\_password | vSphere password | `string` | n/a | yes |
| vsphere\_server | vSphere server | `string` | n/a | yes |
| vsphere\_user | vSphere username | `string` | n/a | yes |

## Outputs

No output.

<!--- END_TF_DOCS --->
