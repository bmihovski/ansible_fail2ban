Role Name
=========

Create and test fail2ban rule

Requirements
------------

Ansible 2.1

Role Variables
--------------

filter_conf: - ( filename for new filter )
filter_regex: - ( filter regex content )
create: - Bool ( create the the )
test_it: Bool ( test the filter )
log_file_to_check: ( log file to validate the template )

defaults/main.yml

fail2ban_conf_path: ( path to file2ban conf dir )

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- name: Implement postfix fail2ban rule
  hosts: server1
  gather_facts: false
  roles:
    - create_filter
  vars:
    - filter_conf: postfix_unknown.conf
    - filter_regex: "^.* postfix/smtpd\\[.*\\]: connect from unknown\\[<HOST>\\]$"
    - create: true
    - test_it: true
    - log_file_to_check: /var/log/syslog
    
License
-------

BSD

Author Information
------------------

Boyan Mihovski https://github.com/bmihovski/
