Vagrant
=======

An Ansible Role that installs and configures [Vagrant](https://www.vagrantup.com/).

Requirements
------------

This role has only been tested on Ubuntu 20.04.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml)

    vagrant_plugins: []

A list of Vagrant plugins to install.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      
      vars:
        vagrant_plugins:
          - vagrant-disksize

      roles:
         - orjangj.virtualization.vagrant

License
-------

MIT / BSD
