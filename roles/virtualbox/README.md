Virtualbox
==========

An Ansible Role that installs and configures [VirtualBox](https://www.virtualbox.org/)

Requirements
------------

This role has only been tested on Ubuntu 20.04.

> Does not work with secure boot enabled

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml)

    virtualbox_version: 6.1

The VirtualBox version to install.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all

      roles:
         - orjangj.virtualization.virtualbox

License
-------

MIT / BSD
