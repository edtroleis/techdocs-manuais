# Podman machine

No Windows e no macOS os containers rodam numa VM Linux: a **Podman machine**.

```bash
podman machine init --cpus 4 --memory 8192 --disk-size 60
podman machine start
podman machine list
```

| Opção | Recomendação |
|-------|--------------|
| CPUs | Metade dos núcleos da máquina |
| Memória | 8 GB para desenvolvimento típico |
| Rootful | Desligado (padrão); ligue só se precisar de portas < 1024 |

Pelo Podman Desktop: **Settings → Resources → Podman → Create new**.

!!! tip "Dentro do WSL"
    Se você já trabalha numa distribuição WSL, pode instalar o Podman direto nela e não usar
    a Podman machine.
