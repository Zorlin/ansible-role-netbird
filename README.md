ansible-role-netbird
====================

This is an Ansible role that installs [Netbird](https://netbird.io/) automatically, including registering nodes with Netbird with no user interaction needed.

Requirements
------------

* Ansible 2.10+ or later.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

* `netbird_setup_key` - A valid API key for registering nodes with Netbird.io. Required if `netbird_register` is set to "true" (default).
* `netbird_register` - Defaults to "true"; determines whether or not Netbird will automatically register nodes. If set to "false", this role will simply install Netbird.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
---
- name: Install Netbird
  hosts: servers
  
  vars:
    netbird_setup_key: "not-a-real-api-key"

  roles:
  - { role: zorlin.netbird }
```

Credits and License
-------------------

Copyright (c) 2022 Benjamin Arntzen & Protocol Labs. Made available under the MIT License.