# Simple WEB APP by Flask and Deploy on Kubernetes

This is a web application project which is written by `Flask`.
Also there are some practices regarding creating infrastructure as code (Terraform, Ansible, Vagrant)
and installing kubernetes cluster (via ansible-playbook) and preparing CI/CD pipline for deploying the application on k8s cluster.

### Create Container
Create a container from the image.
```
docker run --rm --name my-flask -d -p 8080:8080 flaskcd
```

Now visit http://localhost:8080

### Verify the running container
Verify by checking the container ip and hostname (ID):
```
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' my-flask
docker inspect -f '{{ .Config.Hostname }}' my-flask
```
### Terraform

```
terraform destroy -var-file=dev.tfvars
```

```
terraform plan -var-file=dev.tfvars -out devtfplan.out
#
terraform apply "devtfplan.out"
```
### Ansible

### Deploy on Kubernetes

### To Do
<details> 
<summary> Preview</summary>

- [ ] Adding DB (`MySQL`) and connecting the application to it and assing some forms in application.
- [ ] Creating a `StatefulSet` for `MySQL` for deploying it on Kubernetes.
    - [ ] Configure clustring for `MySQL` in Kubernetes.
- [ ] Implementing `ROOK` or `longhorn` as a `StorageClass` in Kubernetes.
- [ ] Configuring `provision` in `Terraform` for using `ansible-playbook` for installing Kubernetes.
- [ ] Creating `helm` chart for DB and APP.

</details>