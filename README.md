Upgrade SLES 12 to SLES 12SP5
=========

Playbook for SLES 12 upgrade from SP1 (or SP2, or SP3, or SP4) to SP5.

Requirements
------------

Ansible server:
- Ansible 2.7+

Target machine(s):
- Machine is subscribed to the SUSE portal or local SMT
- Zypper mirror needs to be configured, so system can download the packages
- SUSE 12SP1-12SP4
- Minimum 1GB free on /usr partition

Role Variables
--------------

- zypper_mirror_url (defaults/main.yml: "https://updates.suse.com")


Example Playbook
----------------

    - hosts: all
      become: yes
      become_user: root
      become_method: sudo
      gather_facts: true
      ignore_errors: no
      
      roles:
        - upgrade-sles12-to-12sp5

Author Information
------------------

Darko Drazovic \
LinkedIn: https://www.linkedin.com/in/darkodrazovic \
Personal: https://darkodrazovic.in.rs \
Blog: https://kompjuteras.com \
GitHub: https://github.com/darkodrazovic