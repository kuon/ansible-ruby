Ruby
====

Install ruby and rbenv.

Requirements
------------

Tested with Ansible 1.6 or higher.

Role Variables
--------------

- `ruby_install_path` - Path where ruby will be installed, default to `/srv`
- `ruby_version` - Full version of the ruby to install (MRI) default to `2.2.2`

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: kuon.ruby, ruby_install_path: '/opt' }

License
-------

MIT


