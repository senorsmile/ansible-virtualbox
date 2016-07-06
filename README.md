# ansible role: virtualbox

[![Build Status](https://travis-ci.org/hubisan/ansible-virtualbox.svg?branch=master)](https://travis-ci.org/hubisan/ansible-virtualbox)

An Ansible role for installing VirtualBox on Ubuntu.

## Requirements

This role requires Ansible 2.0 or higher.

Tested on Ubuntu 12.04 and 14.04. Should work on all Ubuntu versions >= 12.04.

## Role Variables

Default variables:

``` yaml
---
# defaults file for virtualbox
virtualbox_version: "5.0"
virtualbox_install_dkms: no
```

## Dependencies

None.

## Example Playbook

Install VirtualBox:
``` yaml
- hosts: all
  roles:
    - { role: hubisan.virtualbox }
```

Install specific version of VirtualBox and virtualbox-dkms:
``` yaml
- hosts: all
  roles:
    - { role: hubisan.virtualbox, virtualbox_version: 4.2, virtualbox_install_dkms: yes }
```

## Installation

### From Ansible Galaxy

``` shell
ansible-galaxy install hubisan.virtualbox
```

### Installation From Github directly

To download from GitHub directly add requirements.yml:

``` yaml
# Install role from GitHub
- name: virtualbox
  src: https://github.com/hubisan/ansible-virtualbox
```

and add this to your playbook:

``` yaml
- name: run ansible galaxy
  command: ansible-galaxy install -r requirements.yml --ignore-errors
```

## License

MIT

## Author Information

Daniel Hubmann
