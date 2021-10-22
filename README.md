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

    terraform_architecture: 'amd64'    # enum, one of 386|amd64|arm

    terraform_version: '0.12.24'

    terraform_binary_dir_path: "/usr/local/bin"

    terraform_plugin_urls: []

Dependencies
------------

None

Example Playbook
----------------

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
