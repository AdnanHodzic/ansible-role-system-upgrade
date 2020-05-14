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

Donate
-------

Since I'm working on this project in free time, please consider supporting this project by making a donation of any amount!

##### PayPal
[![paypal](https://www.paypalobjects.com/en_US/NL/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=7AHCP5PU95S4Y&item_name=Contribution+for+work+on+containerized-wordpress-project&currency_code=EUR&source=url)

##### BitCoin
[bc1qlncmgdjyqy8pe4gad4k2s6xtyr8f2r3ehrnl87](bitcoin:bc1qlncmgdjyqy8pe4gad4k2s6xtyr8f2r3ehrnl87)

[![bitcoin](https://foolcontrol.org/wp-content/uploads/2019/08/btc-donate-displaylink-debian.png)](bitcoin:bc1qlncmgdjyqy8pe4gad4k2s6xtyr8f2r3ehrnl87)

