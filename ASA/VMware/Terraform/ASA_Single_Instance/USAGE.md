# Usage
<!--- BEGIN_TF_DOCS --->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| null | n/a |
| vsphere | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| cluster | Cluster name | `string` | n/a | yes |
| datacenter | Datacenter name | `string` | n/a | yes |
| datastore | Datastore name | `string` | n/a | yes |
| day0\_config | Day0 Config file | `string` | n/a | yes |
| host | Host IP/hostname | `string` | n/a | yes |
| hostname | ASAv Hostname | `string` | `"asav-terraform"` | no |
| inside\_network | Inside interface network | `string` | n/a | yes |
| mgmt\_network | Management interface network | `string` | n/a | yes |
| outside\_network | Outside interface network | `string` | n/a | yes |
| ovf\_path | Path to asav-vi.ovf | `string` | n/a | yes |
| password | Login Password | `string` | n/a | yes |
| userid | Login User ID | `string` | n/a | yes |
| vsphere\_server | VCenter hostname or IP | `string` | n/a | yes |

## Outputs

No output.

<!--- END_TF_DOCS --->
