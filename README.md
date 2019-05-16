[![Build Status](https://travis-ci.com/oasis-roles/ocp_configure_users.svg?branch=master)](https://travis-ci.com/oasis-roles/ocp_configure_users)

ocp_configure_users
===========

Basic description for ocp_configure_users

Requirements
------------

Ansible 2.4 or higher

Red Hat Enterprise Linux 7 or equivalent

Valid Red Hat Subscriptions

Role Variables
--------------

Currently the following variables are supported:

### General

* `ocp_configure_users_become` - Default: true. If this role needs administrator
  privileges, then use the Ansible become functionality (based off sudo).
* `ocp_configure_users_become_user` - Default: root. If the role uses the become
  functionality for privilege escalation, then this is the name of the target
  user to change to.

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: ocp_configure_users-servers
  roles:
    - role: oasis_roles.ocp_configure_users
```

License
-------

GPLv3

Author Information
------------------

Author Name <authoremail@domain.net>