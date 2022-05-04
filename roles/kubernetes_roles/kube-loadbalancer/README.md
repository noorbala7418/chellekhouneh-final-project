# Kubernetes-Loadbalancer

Set `private_ip` var in `masters` group -> `hosts` file. 

Example:

```yml
all:
  children:
    masters:
      hosts:
        master1:
          ansible_host: 1.2.3.4
          private_ip: 192.168.1.10/24 # THIS SECTION!
          ansible_user: ubuntu
          ansible_become_method: sudo
```

default vars:

```yml
haproxy_conf_dir: "/opt/haproxy"
haproxy_img_name: "dockerhub.ir/haproxy:2.4.16-alpine3.15"
```