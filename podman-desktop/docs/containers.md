# Containers

```bash
podman run --rm quay.io/podman/hello
podman run -d --name web -p 8080:80 docker.io/library/nginx:alpine
podman ps
podman logs web
podman stop web && podman rm web
```

## Imagens

```bash
podman build -t meu-app:dev .
podman images
podman image prune
```

## Registro corporativo

```bash
podman login registry.exemplo.com
podman pull registry.exemplo.com/base/python:3.12
```

Use sempre imagens de **origem aprovada** e com tag fixa.
