Role Name
=========

Check and assert file content

Requirements
------------

Ansible 2.1

Role Variables
--------------

file_to_check: ( file to check )  
file_content_to_check: ( file content to check )

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- name: Check and assert filter file content
  include_role:
    name: check_file_content
  vars:
    file_to_check: '/tmp/test'
    file_content_to_check: 'test content'

License
-------

BSD

Author Information
------------------

Boyan Mihovski https://github.com/bmihovski/
