ansible-usersmgt
=========

[![Build Status](https://travis-ci.org/galexrt/ansible-usersmgt.svg?branch=master)](https://travis-ci.org/galexrt/ansible-usersmgt)

An user management role for Ansible.

Requirements
------------

No special requirements.

Role Variables
--------------

Please check the file `default/all.yml` to see what variables are available.
```
sudoers_file: /etc/sudoers

users:
  - name: "USER_NAME"
    uid: UNIQUE_UID # optional
    group: "wheel" # primarygroup
    groups: [] # secondary groups (optional)
    comment: "FULL_NAME" # optional
    non_unique: yes # optional
    system: no # optional
    createhome: yes # optional

users_sudo:
  - name: "%wheel"
    mode: "ALL"
  - name: example1
    mode: "ALL"
  - name: example2
    mode: "NOPASSWD:ALL"

users_groups:
  - name: example
    gid: 420
    system: yes
  - name: example2
    gid: 1337

# Set "global" umask
users_umask_set: false
users_umask: "077"
```

Dependencies
------------

No dependencies.

Example Playbook
----------------

To use this role you add the following as the name of the role:

    - hosts: all
      roles:
        - { role: galexrt.usersmgt }

License
-------

Apache License Version 2.0

Author Information
------------------

If you have problems with the role, feel free to create an issue on Github or contact me by mail.

Examples
--------
For examples on how to use this Ansible role refer to the [EXAMPLES.md](EXAMPLES.md).

ToDo List
--------
- [ ] Write tests
