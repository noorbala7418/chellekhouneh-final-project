# Kubernetes Master Init

Runs `Kubeadm init ....` on master initializer node.

default vars:

```yml
pod_network_cidr: "10.244.0.0/16"
kubeadm_img_repository: "k8s.noorbala7418.ir"
kuber_image_version: "v1.23.6"
```