GlusterFS Server
=========

Setup GlusterFS servers using Ansible Tower.

Requirements
------------

Atleast one free unused extra disk per system
root like access for Ansible tower

Role Variables
--------------
defaults/main.yml
- gluster_package_version: '37'
- gluster_filesystem: "xfs"
- gluster_brick_dir: "/glusterfs/brick1"
- gluster_volume_name: "tri-repvol01"
- gluster_replicas: "3"


Dependencies
------------

none

Example Playbook
----------------
---
# This playbook deploys the GlusterFS Server application

- hosts: glusterfs-servers
  strategy: linear
  gather_facts: true
  roles:
    - role: gluster-server

License
-------

GPLv2

Author Information
------------------

More info about GlusterFS here:
https://gluster.readthedocs.io/en/latest/
