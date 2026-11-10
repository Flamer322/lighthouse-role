# LightHouse Ansible Role

An Ansible role for deploying
[VKCOM LightHouse](https://github.com/VKCOM/lighthouse)
for Nginx.

## Requirements

- Ansible >= 2.12
- Ubuntu 24.04
- Internet access

## Role Variables

| Variable | Default | Description |
| --- | --- | --- |
| `lighthouse_repository` | VKCOM/lighthouse | Git repository |
| `lighthouse_version` | `master` | Git branch or tag |
| `lighthouse_directory` | `/opt/lighthouse-master` | Installation directory |
| `lighthouse_server_name` | `_` | Nginx server name |

## Example Playbook

```yaml
---
- name: Install LightHouse
  hosts: lighthouse
  become: true
  roles:
    - lighthouse
