Ansible Mount Role
==================
[![Build Status](https://travis-ci.org/michaelrigart/ansible-role-mount.svg)](https://travis-ci.org/michaelrigart/ansible-role-mount)

An ansible role for mounting devises.


Role Variables
--------------

mount_devises: list of dictionaries holding all devises that need to be mounted.
- name: /
  src: /dev/mapper/root
  fstype: ext4
  opts: noatime,errors=remount-ro
  state: mounted
  dump: 0
  passno: 1


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: MichaelRigart.mount }

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>
