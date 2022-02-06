# Ansible collection for virtualization

This collection includes Ansible roles and content to help with virtualization automation.

Roles included in this collection (click on the link to see the role's README and documentation):

  - `orjangj.virtualization.docker` ([documentation](https://github.com/orjangj/ansible-collection-virtualization/blob/master/roles/docker/README.md))
  - `orjangj.virtualization.vagrant` ([documentation](https://github.com/orjangj/ansible-collection-virtualization/blob/master/roles/vagrant/README.md))
  - `orjangj.virtualization.virtualbox` ([documentation](https://github.com/orjangj/ansible-collection-virtualization/blob/master/roles/virtualbox/README.md))

## Supported distributions

* Ubuntu 20.04

## Installation

Currently not installable from Ansible Galaxy. Historically this collection has been for personal use only.

Install using `ansible-galaxy` with git url:

```
ansible-galaxy collection install git+https://github.com/orjangj/ansible-collection-virtualization.git
```

Or include this collection in your playbook's `requirements.yml` file:

```
---
collections:
  - name: https://github.com/orjangj/ansible-collection-virtualization.git
    type: git
    version: master
```

## Usage

Here's an example playbook which installs Docker, and adds the ansible user to the Docker group:

```yaml
- hosts: all

  vars:
    docker_users:
      - "{{ ansible_user_id }}"

  roles:
    - orjangj.virtualization.docker
```

## License

MIT
