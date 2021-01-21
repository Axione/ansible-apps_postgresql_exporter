# Ansible Role: ansible-apps_postgresql_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_postgresql_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_postgresql_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_postgresql_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_postgresql_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_postgresql_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_postgresql_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_postgresql_exporter.svg)](https://github.com/lotusnoir/ansible-apps_postgresql_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_postgresql_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_postgresql_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_postgresql_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_postgresql_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_postgresql_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_postgresql_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_postgresql_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_postgresql_exporter)

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
