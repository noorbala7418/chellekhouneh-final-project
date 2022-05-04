# Kubernetes Bootstrap Role

- Enable Kernel Modules for k8s.
- Install `kubectl`, `kubeadm`, `kubelet` base on `kube_component_version` variable.

default vars:

```yml
kube_component_version: "1.23.6-00"
```