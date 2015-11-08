mysql
========

[![Build Status](https://drone-opsdev.rax.io/github.com/rack-roles/mysql/status.svg?branch=master)](https://drone-opsdev.rax.io/github.com/rack-roles/mysql)

This is a basic role to install and configure MySQL. This role does not manage any database imports or dumps. Please handle that outside of this role.

Requirements
------------

No external requirements.

Role Variables
--------------

## Mandatory
These values have to be overridden.
* `mysql_replication_password`
* `mysql_master_host` The ip address slaves should access the master.
* `mysql_configure_slave` When setting up replication for the first time, set this to True.

## Standard
* `mysql_bind_address` Defaults to 127.0.0.1
* `mysql_port` Defaults to 3306
* `mysql_root_password` Defaults to a random value

## Replication
* `mysql_replication` False
* `mysql_replication_role` Set either `master` or `slave`.
* `mysql_replication_user` replicant
* `mysql_log_bin` "/var/lib/mysql/binary-log"
* `mysql_expire_logs_days` 5
* `mysql_relay_log` "/var/lib/mysql/relay-log"
* `mysql_relay_log_space_limit` "4G"
* `mysql_server_id`

Dependencies
------------

`Rackspace_Automation.holland` (Optional)

Example Playbook
-------------------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: Rackspace_Automation.mysql, x: 42 }

License
-------

BSD

Author Information
------------------

[Rackspace - the open cloud company](http://rackspace.com)

Ask about our DevOps Automation Service - [www.rackspace.com/devops](http://rackspace.com/devops)
