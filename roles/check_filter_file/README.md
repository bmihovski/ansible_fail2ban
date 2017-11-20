Role Name
=========

Check filter file exists and it's content

Requirements
------------

Ansible 2.1

Role Variables
--------------

filter_conf: ( filter file to check )
content_to_check: ( filter content to check )  


Dependencies
------------

role: check_file_content

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- name: Check filter file
  include_role:
    name: check_filter_file 
  vars:
    filter_conf_file: '/tmp/test.conf'
    content_to_check: 'test_content'

License
-------

BSD

Author Information
------------------

Boyan Mihovski https://github.com/bmihovski/
