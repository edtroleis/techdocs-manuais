# Compose e Kubernetes

## Compose

```bash
podman compose up -d
podman compose down
```

## Pods

```bash
podman pod create --name app -p 8080:80
podman run -d --pod app docker.io/library/nginx:alpine
```

## Gerar YAML de Kubernetes

```bash
podman kube generate app > app.yaml
podman kube play app.yaml
```

O Podman Desktop também integra com clusters locais (Kind, Minikube) em **Settings → Resources**.
