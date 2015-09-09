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

Variables
----------------

Most variables are stored in the other playbooks with the follwing exceptions:

```
duplicity_download_path: where you want to put the tar.gz file
duplicity_download_url: the Full URL to the tar.gz for the 0.7 file.
duplicity_version: Version of Duplicity
```

```
duplicity_src: The list of directories to backup
duplicity_dest: The swift://URL of the backup site
duplicity_keep: Used for the "--full-if-older-than" switch in Duplicity
```
...

Author Information
------------------

Blake Carver, Mark Cooper.

---
