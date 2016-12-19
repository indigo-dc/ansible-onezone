Onezone 
=========

Onezone is a Onedata service enabling federation of storage providers and user authentication. 

You can use this Ansible role to install Onezone on a single machine. Furthermore this role allows you to
- check if machine meets minimal hardware req., needed ports are open and FQDN is properly resolved
- install, configure and uninstall Onezone
- uninstall Onezone
- stop Onezone services

Requirements
------------

This role requires version Ansible 2.2.0 or newer.

Role Variables
--------------

This role does not include variables that user need to define prior to using the role. All variables that might be of interest are located and documented in: defaults/main.yml

Dependencies
------------

This role has no dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

~~~
- hosts: all
  become: yes
  
  roles:
    - { role: onezone, requirements_check: true, onezone_install: true, onezone_configure: true, onezone_restart: true, onezone_uninstall: true} # This illustrates all possible stages that can be run with this playbook
    # - { role: onezone } # by default only options onezone_configure and onezone_install will run, if no options are specified
~~~

License
-------

MIT