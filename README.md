# ansible-apps_postgresql_exporter

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_postgresql_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_postgresql_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_postgresql_exporter.svg)](https://github.com/lotusnoir/ansible-apps_postgresql_exporter/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_postgresql_exporter?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_postgresql_exporter)
[![downloads](https://img.shields.io/ansible/role/d/52267)](https://galaxy.ansible.com/lotusnoir/apps_postgresql_exporter)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/52267)](https://galaxy.ansible.com/lotusnoir/apps_postgresql_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

## Description

Deploy [postgresql_exporter](https://github.com/wrouesnel/postgres_exporter) to expose postgresql metrics to prometheus.
## Requirements

none

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_postgresql_exporter
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_postgresql_exporter

## Grafana Dashboard

You can find a grafana dashboard [here](https://grafana.com/grafana/dashboards/13556)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
