[![Build Status](https://travis-ci.com/oasis-roles/ocp_configure_users.svg?branch=master)](https://travis-ci.com/oasis-roles/ocp_configure_users)

ocp\_configure\_users
===========

Creates and configures OpenShift users against a cluster configured to use
htaccess based authentication.

Requirements
------------

Ansible 2.4 or higher

Red Hat Enterprise Linux 7 or equivalent

Valid Red Hat Subscriptions

Role Variables
--------------

Currently the following variables are supported:

### General

* `ocp_configure_users` - Default: []. A list of objects defining the users to
  be created. Form should be `{"username": "myuser", "password": "mypass",
  "role": "cluster-admin"}` for each element in the list. All three fields are
  required.
* `ocp_configure_users_htpasswd_path` - Default: /etc/origin/master/htpasswd. Path
  to the htpasswd file that contains authorization for OpenShift users.
* `ocp_configure_users_become` - Default: true. If this role needs administrator
  privileges, then use the Ansible become functionality (based off sudo).
* `ocp_configure_users_become_user` - Default: root. If the role uses the become
  functionality for privilege escalation, then this is the name of the target
  user to change to.

Dependencies
------------

A configured OpenShift cluster that utilizes htpasswd authentication with access
to the masters of the cluster.

Example Playbook
----------------

```yaml
- hosts: masters
  roles:
    - role: oasis_roles.ocp_configure_users
      ocp_configure_users:
        - username: admin
          password: s0m3p4ssw0rd
          role: cluster-admin
```

License
-------

GPLv3

Author Information
------------------

Greg Hellings <greg.hellings@gmail.com>
