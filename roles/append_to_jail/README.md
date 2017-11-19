Role Name
=========

Apply and test fail2ban rule to jail.conf

Requirements
------------

Ansible 2.4

Role Variables
--------------

jail_conf_file: - ( filename of jail configuration file )
log_file_to_check: - ( log file to validate the template )
filter_name: - ( filter name to be applied )
create: - Bool ( create the the )
test_it: Bool ( test the filter )

defaults/main.yml

fail2ban_conf_path: ( path to file2ban conf dir )
jail_conf_rule_content: ( jail configuration to be applied )

handlers/main.yml
update fail2ban: - ( load the new filter to fail2ban )

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- name: Apply postfix fail2ban rule to jail conf
  hosts: server1
  gather_facts: false
  roles:
    - append_to_jail
  vars:
    - jail_conf_file: jail.conf
    - log_file_to_check: /var/log/syslog
    - filter_name: postfix_unknown
    - create: true
    - test_it: true
    
License
-------

BSD

Author Information
------------------

Boyan Mihovski https://github.com/bmihovski/
