Role Name
=========

This role installs duplicity from the duplicity source code at http://duplicity.nongnu.org/
It uses the Duplicity 0.7 Series.
main.yml installs dependencies using apt. It then uses pip to install python-swift & keystone.
It then downloads and installs Duplicity from the tar.gz source from launchpad.
Logging is done to /var/log/duplicity.log
The actual backup scripts are kept in the corresponding playbooks, along with cron jobs & keys.

Example Playbook
----------------

`ansible-playbook -i ./inventory/hosts ./duplicity.yml -K --tags install`

...

Author Information
------------------

Blake Carver, Mark Cooper.

---
