Ansible Mount Role
==================
[![Build Status](https://semaphoreci.com/api/v1/projects/1a67bd32-ca28-4baa-afa3-6329dae67e85/459474/badge.svg)](https://semaphoreci.com/michaelrigart/ansible-role-mount) [![Build Status](https://travis-ci.org/michaelrigart/ansible-role-mount.svg)](https://travis-ci.org/michaelrigart/ansible-role-mount)

An ansible role for mounting devices.

Role Variables
--------------

```yaml
# list of dictionaries holding all devices that need to be mounted.
mount_devices:
  - name: /                         # NO default
    src: /dev/mapper/root           # NO default
    fstype: ext4                    # NO default
    opts: noatime,errors=remount-ro # default: "defaults"
    state: present                  # default: "mounted"
    dump: 0                         # default: "0"
    passno: 1                       # default: "0"
    fstab: /etc/fstab               # default: "/etc/fstab"
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
