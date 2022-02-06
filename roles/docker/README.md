Docker
======

Ansible Role that installs and configures [Docker](https://www.docker.com)

Requirements
------------

This role has only been tested on Ubuntu 20.04.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml)

    virtualization_docker_users: []

A list of users to add to the docker group.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      
      vars:
        docker_users:
          - {{ ansible_user_id }}

      roles:
         - orjangj.virtualization.docker

License
-------

MIT / BSD
