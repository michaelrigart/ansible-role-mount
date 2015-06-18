Ansible Mount Role
==================
[![Build Status](https://semaphoreci.com/api/v1/projects/1a67bd32-ca28-4baa-afa3-6329dae67e85/459474/badge.svg)](https://semaphoreci.com/michaelrigart/ansible-role-mount) [![Build Status](https://travis-ci.org/michaelrigart/ansible-role-mount.svg)](https://travis-ci.org/michaelrigart/ansible-role-mount)

An ansible role for mounting devices.

Role Variables
--------------

```yaml
# list of dictionaries holding all devices that need to be mounted.
mount_devices:
  - name: /
    src: /dev/mapper/root
    fstype: ext4
    opts: noatime,errors=remount-ro
    state: mounted
    dump: 0
    passno: 1
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - { role: MichaelRigart.mount, sudo: Yes }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>
