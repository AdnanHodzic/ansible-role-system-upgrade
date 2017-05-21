Ansible Role: (Ubuntu) System Upgrade
=========

**Perform upgrade of all software packages on Ubuntu host.**

This Ansible role will perform upgrade of all software packages on Ubunty host. After which it will reboot host (only if required). If reboot was performed, it'll wait until host is back-up.

  * Update APT cache
  * Check if there are any available updates
  * Perform upgrade of all packages to the latest version (dist)
  * Check if a reboot is required, if it is reboot the host/server
  * Wait for server to come back after reboot, and report once it's back-up and running.
  
This role was created as part of [containerized-wordpress-project](https://github.com/AdnanHodzic/containerized-wordpress-project)
  

Requirements
------------

None.

Role Variables
--------------

None.

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  remote_user: ubuntu # optional
  gather_facts: yes
  become: yes

  roles:
    - { role: AdnanHodzic.system-upgrade }
```

License
-------

GPLv3
