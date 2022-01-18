# Kubernetes Labratory

This is a 3-node-cluster Kubernetes that uses `k3s`.
This project was prepared for *two type of vagrant prividers*:

### Requirement

1. Ansible
2. Vagrant

### How is it work?
Run below command:
```bash
vagrant up
```
### Kubeconfig

```
scp vagrant@master_ip:~/.kube/config ~/.kube/config
```