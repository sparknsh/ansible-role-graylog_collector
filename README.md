# Ansible Role: Graylog Collector

#### Version: 1.0.1

[![pipeline status](https://gitlab.com/sparknsh/ansible-role-graylog-collector/badges/master/pipeline.svg)](https://gitlab.com/sparknsh/ansible-role-graylog-collector/commits/master)
[![Ansible Role](https://img.shields.io/ansible/role/30023.svg)](https://galaxy.ansible.com/sparknsh/graylog_collector)
[![Ansible Role](https://img.shields.io/ansible/role/d/30023.svg)](https://galaxy.ansible.com/sparknsh/graylog_collector)

Development of this project is managed in a private repository then pushed out to [GitLab](https://gitlab.com/sparknsh/ansible-role-graylog-collector) and [GitHub](https://github.com/sparknsh/ansible-role-graylog-collector) when we have a new version for you. If you have any issues please contact [sparknsh](https://www.sparknsh.com/contact?type=issue&name=ansible-role-graylog-collector)

## Role Variables

Use this variable to specify the the version of sidecar to install

```yaml
graylog_collector_version: 0.1.6
```

Set the url endpoint of your Graylog server

```yaml
graylog_collector_server_url: http://127.0.0.1:9000/api/
```

Use this variable to set a custom name for the server in Graylog. The default is the hostname

```yaml
graylog_collector_node_id:
```

Set tags for the server you're installing sidecar on

```yaml
graylog_collector_tags: []
```

#### Example

```yaml
graylog_collector_version: 0.1.6
graylog_collector_server_url: http://graylog:9000/api/
graylog_collector_tags:
  - linux
  - nginx
  - php
  - mysql
```

## Example Playbook

```yaml
- hosts: all
  vars_files:
    - vars/main.yml
  roles:
     - { role: sparknsh.graylog_collector }
```

## License

MIT

## Author Information

This role was created in 2018 by [sparknsh](https://www.sparknsh.com) at [Rebel Media, Inc.](https://www.rebelmedia.io/)
