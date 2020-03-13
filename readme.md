# MariaDB Ansible Role

This ansible role installs a configurable MariaDB version on a Ubuntu machine.

## Customization

There are a handful of varialbes which can be used to configure how the MariaDB is installed.

```yaml
mariadb_version: "10.2" # the version of MariaDB to install

mariadb_root_password: 123455

mariadb_bind_address: 0.0.0.0

# can be multiple users
mariadb_users:
  - name: "test"
    password: "password"
    host: "%"
    database: "test"

# can be multiple databases
mariadb_databases:
  - name: "test"
    collation: utf8_general_ci
    encoding: utf8
```