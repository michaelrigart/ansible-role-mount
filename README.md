Ansible Mount Role
==================

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
    - { role: MichaelRigart.mount, become: true }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>
