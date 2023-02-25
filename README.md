Role Name
=========

A role to install Vector.

- Gets the archive, 
- Provides the necessary symlinks, 
- Generates a config based on a template (the config sends dmesg logs to the clickhouse-01 node)
- Enables and starts the service

Requirements
------------

No additional requirements

Role Variables
--------------

No changable variables provided.


Example Playbook
----------------

    - hosts: vector
      roles:
         - vector-role

License
-------

MIT

