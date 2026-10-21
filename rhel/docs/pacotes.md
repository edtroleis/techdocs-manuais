# Pacotes

```bash
sudo dnf repolist
sudo dnf search podman
sudo dnf install -y podman git vim-enhanced
sudo dnf update -y
sudo dnf history
```

| Repositório | Conteúdo |
|-------------|----------|
| BaseOS | Sistema operacional base |
| AppStream | Aplicações, linguagens e ferramentas |
| CodeReady Builder | Pacotes de desenvolvimento adicionais |

```bash
sudo subscription-manager repos --enable codeready-builder-for-rhel-9-$(arch)-rpms
```

!!! warning "Repositórios de terceiros"
    Repositórios fora da Red Hat (como EPEL) só com aprovação, conforme a política de software.
