# Ansible Galaxy role for configure /etc/hosts file.

![Build Status](https://github.com/leadlineit/ansible-role-hosts/actions/workflows/ansible-galaxy-ci.yml/badge.svg)
[![Galaxy Role](https://img.shields.io/badge/Ansible--Galaxy-leadlineit.hosts-blue.svg?logo=ansible&logoColor=white)](https://galaxy.ansible.com/leadlineit/hosts/)

This role helps to configure the /etc/hosts file.

Supported OSes
--------------
- Debian 12 (bookworm)
- Debian 11 (bullseye)
- Debian 10 (buster)
- Debian 9 (stretch)

Requirements
------------

This role requires Ansible 2.11 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

```yaml
---
hosts:
  - ip: 172.16.1.1
    host: test.example.lcl
    comment: test host
  - ip: 172.16.1.4
    host: git.example.lcl
```

The 'comment' variable is not obligatory.  
You can use the value 'empty' in comment variable to add a blank line.

Some instances with zabbix-proxy or other monitoring tools needs hosts_custom option:

```yaml
---
hosts_custom: yes
```

Some instances without fqdn hostname needs hosts_fqdn option:

```yaml
---
hosts_fqdn: app1.example.com
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
    - { role: leadlineit.hosts, tags: hosts }
```

License
-------

BSD

Author Information
------------------

This role was created by Stas Stavnichuk.
