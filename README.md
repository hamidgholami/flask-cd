# Simple WEB APP by Flask and SQLite and Deploy on Kubernetes

A load-balanced (public) REST API serving some json from an existing (loaded) database

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