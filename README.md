Role for managing [parca](https://parca.dev)

Heavy WIP but works.

For possible settings and format look at [example config](https://raw.githubusercontent.com/parca-dev/parca/main/parca.yaml)

## Compatibility
This role is compatible with any modern systemd-based distro.

## Role Variables
| Variable name                    | Default value | Description                                        |
| -------------------------------- | ------------- | -------------------------------------------------- |
| parca_server_version             | `0.4.1`       | version of parca                                   |
| parca_server_system_user         | `parca`       | user for running parca                             |
| parca_server_system_group        | `parca`       | group for running parca                            |
| parca_server_port                | `7070`        | listen port for parca                              |
| parca_server_config              | see defaults  | YAML with parca config block                       |
| parca_server_scrape_configs      | see defaults  | YAML with scrape configs                           |
| parca_server_retention           | 1h            | Samples retention time                             |
| parca_server                     | `false`       | If set to true, will install server                |

## Settings
By default this role does nothing.
If you want to install parca, set parca_server to true in group/host vars.
With default scrape config parca will scrape itself.

## TBD

* Agent support
* Proper readme
* Maybe tests
