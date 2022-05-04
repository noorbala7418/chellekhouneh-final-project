# Kubernetes Custom Image Downloader

Used for download kubernetes Master node require images.

images:

- k8s.gcr.io/kube-apiserver:v1.23.6
- k8s.gcr.io/kube-proxy:v1.23.6
- k8s.gcr.io/kube-scheduler:v1.23.6
- k8s.gcr.io/kube-controller-manager:v1.23.6
- k8s.gcr.io/etcd:3.5.1-0
- k8s.gcr.io/coredns/coredns:v1.8.6
- k8s.gcr.io/pause:3.6

default vars:

```yml
kubeadm_img_repository: "k8s.noorbala7418.ir"
kuber_image_version: "v1.23.6"
```