# nephelaiio.k8s

[![Build Status](https://github.com/nephelaiio/ansible-role-k8s/workflows/Molecule/badge.svg)](https://github.com/nephelaiio/ansible-role-k8s/actions)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-nephelaiio.k8s-blue.svg)](https://galaxy.ansible.com/nephelaiio/k8s/)

An [ansible role](https://galaxy.ansible.com/nephelaiio/k8s) to install and configure k8s

## Role Variables

Please refer to the [defaults file](/defaults/main.yml) for an up to date list of input parameters.

## Dependencies

### System

The below requirements are needed on the host that executes this module.
* Linux 64 bit OS
* kubectl binary is available on PATH

### Python

The below requirements are needed on the host that executes this module.

* kubernetes = "^24.2.0"
* openshift = "^0.13.1"

### Ansible

The below python roles are needed on the host that executes this module:

* nephelaiio.plugins

## Example Playbook

``` yaml
---
- name: Deploy local kind cluster

  hosts: localhost

  gather_facts: false
  
  roles:

    - nephelaiio.plugins
    - nephelaiio.kind
    - nephelaiio.k8s

```

## Testing

Please make sure your environment has [docker](https://www.docker.com) installed; then test the role from the project root using the following commands

* ` poetry instasll`
* ` poetry run molecule test `

## License

This project is licensed under the terms of the [MIT License](/LICENSE)
