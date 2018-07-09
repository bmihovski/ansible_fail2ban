Role Name
=========

Apply and test fail2ban date regex for multics to /usr/share/fail2ban/server/datedetector.py

Requirements
------------

Ansible 2.4 fail2ban preinstalled

Role Variables
--------------

create: - Bool ( create the filter )
test_it: Bool ( test the filter )

defaults/main.yml

fail2ban_date_checker_path: ( path to file2ban conf dir )

handlers/main.yml
update fail2ban: - ( load the new regex to fail2ban )

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- name: Apply new date parser for multics
  hosts: server1
  gather_facts: false
  roles:
    - fail2ban_regex_date
  vars:
    - create: true
    - test_it: true

License
-------

BSD

Author Information
------------------

Boyan Mihovski https://github.com/bmihovski/
