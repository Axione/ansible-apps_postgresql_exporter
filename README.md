# Ansible Role: ansible-apps_postgresql_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_postgresql_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_postgresql_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__postgresql_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_postgresql_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_postgresql_exporter/tags)

Deploy [postgresql_exporter](https://github.com/wrouesnel/postgres_exporter) to expose postgresql metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `postgresql_exporter_version` | 0.8.0 | postgresql_exporter version |
| `postgresql_exporter_temp_dir` | /tmp | temporary directory to uncompress package |
| `postgresql_exporter_install_dir` | /usr/local/bin | directory to install binary |
| `postgresql_exporter_force_install` | false | force install variable |
| `postgresql_exporter_web_port` | 9106 | postgresql_exporter listen port |

## Examples

	---
	- hosts: apps_postgresql_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_postgresql_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
