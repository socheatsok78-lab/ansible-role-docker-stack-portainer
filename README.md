# About

Ansible Role - Docker Stack for [Portainer](https://www.portainer.io/)

## Role Variables

```yaml
# Ansible Role Options
portainer_edition: ce
portainer_version: 2.21

portainer_stack_state: present # or absent (default: present)
```

## Add to `requirements.yml`

```yaml
roles:
  - name: socheatsok78-lab.docker-stack-portainer
    src: https://github.com/socheatsok78-lab/ansible-role-docker-stack-portainer
    version: main
    scm: git
```

## Use with Ansible

```yaml
- hosts: docker-swarm-manager[0]
  vars:
    portainer_edition: ce
    portainer_version: 2.21
    portainer_stack_state: present
  roles:
    - socheatsok78-lab.docker-stack-portainer
```
