# Instalação

Abra o **PowerShell como administrador**:

```powershell
wsl --install
```

O comando habilita os recursos necessários, instala o kernel do WSL 2 e a distribuição padrão
(Ubuntu). **Reinicie** o computador quando solicitado.

## Já tem WSL instalado?

```powershell
wsl --update
wsl --set-default-version 2
wsl --version
```

!!! warning "WSL 1"
    Garanta que as distribuições estão na versão 2: `wsl -l -v`. Para converter:
    `wsl --set-version <distro> 2`.
