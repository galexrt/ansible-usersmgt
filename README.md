ansible-usersmgt
=========

[![Build Status](https://travis-ci.org/galexrt/ansible-usersmgt.svg?branch=master)](https://travis-ci.org/galexrt/ansible-usersmgt)

An user management role for Ansible.
Requirements
------------

No special requirements.
Role Variables
--------------

Please check the file `vars/all.yml` to see what variables are available.
Dependencies
------------

No dependencies.
Example Playbook
----------------

To use this role you add the following as the name of the role:

    - hosts: all
      roles:
         - { role: galexrt.ansible-usersmgt }

License
-------

Apache License Version 2.0
Author Information
------------------

If you have problems with the role, feel free to create an issue on Github or contact me by mail.
Examples
--------
For examples on how to use this Ansible role refer to the [EXAMPLES.md](EXAMPLES.md).
TODO List
-------
- [x] Configurable SSH key directory (two modes, all in one and per user)
- [ ] Add not_on_hosts and on_hosts to user removal
- [ ] Write tests
