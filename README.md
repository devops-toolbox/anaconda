Role Name
=========

anaconda

[![Build Status](https://travis-ci.org/cmihai-ansible/anaconda.svg?branch=master)](https://travis-ci.org/cmihai-ansible/anaconda)

Ansible galaxy:
---------------

[https://galaxy.ansible.com/devopstoolbox.anaconda](https://galaxy.ansible.com/devopstoolbox.anaconda)

```bash
ansible-galaxy install devopstoolbox.anaconda
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```yaml
anaconda_url: "https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh"
anaconda_path: "~/anaconda3"
anaconda_user: ansible
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install anaconda on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: anaconda is configured
      import_role:
        name: devopstoolbox.anaconda
      vars:
        anaconda_url: "https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh"
        anaconda_path: "~/anaconda3"
        anaconda_user: ansible
      tags: anaconda
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/devopstoolbox.)
