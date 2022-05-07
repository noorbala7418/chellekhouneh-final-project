# Netplan configuration Role
=========

tags:

- netplan_conf


Required vars: 

```yaml
eth1_ip: "192.168.1.12/24"
eth1_enable_gateway: false
eth1_gw_ip: "192.168.1.1"
```

Example Playbook
----------------

```yaml


- hosts: nginx
  vars:
    eth1_ip: 192.168.0.10/24
  become: true
  roles:
    - netplan

```
