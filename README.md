Ansible role: Terraform
=========

![Build & Deploy](https://github.com/Provizanta/ansible-role-terraform/workflows/molecule/badge.svg?branch=master)

Establish and configure Hashicorp Terraform.

Requirements
------------

None

Role Variables
--------------

These variables are defined in [defaults/main.yml](./defaults/main.yml):

    terraform_plugin_urls: []

Additionally, it is possible to define an explicit version to be downloaded and installed:

    terraform_version: '0.12.24'


Dependencies
------------

None

Example Playbook
----------------

To get a default package:

    - name: Converge
      hosts: all
      roles:
        - role: terraform


To get an explicit version:

    - name: Converge
      hosts: all
      vars:
        version: '0.12.24'
      roles:
        - role: terraform
          vars:
            terraform_version: "{{ version }}"
            terraform_binary_dir_path: /usr/bin

License
-------

MIT

Author Information
------------------

Tibor Csóka
