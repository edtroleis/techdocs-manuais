# Configuração

## Recursos da VM: `%UserProfile%\.wslconfig`

```ini
[wsl2]
memory=8GB
processors=4
swap=4GB
networkingMode=mirrored

[experimental]
autoMemoryReclaim=gradual
sparseVhd=true
```

## Por distribuição: `/etc/wsl.conf`

```ini
[boot]
systemd=true

[user]
default=meu-usuario
```

Aplique as mudanças com `wsl --shutdown` e abra a distribuição novamente.

!!! tip "Projetos no filesystem Linux"
    Mantenha o código em `~/code`, não em `/mnt/c/...`. O acesso a arquivos do Windows pelo
    WSL é muito mais lento.
