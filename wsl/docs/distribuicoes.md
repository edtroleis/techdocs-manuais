# Distribuições

```powershell
wsl --list --online          # distribuições disponíveis
wsl --install -d Ubuntu-24.04
wsl -l -v                    # instaladas, estado e versão
wsl --set-default Ubuntu-24.04
```

| Distribuição | Uso recomendado |
|--------------|-----------------|
| Ubuntu LTS | Padrão para desenvolvimento |
| Fedora | Quando o alvo é ecossistema Red Hat |
| RHEL (imagem oficial) | Paridade com servidores RHEL (veja o [Manual de RHEL](http://localhost:3000/docs/default/component/manual-rhel)) |

## Primeiro acesso

Na primeira execução, crie usuário e senha Linux (não precisam ser iguais aos do Windows) e
atualize os pacotes:

```bash
sudo apt update && sudo apt upgrade -y
```

## Backup e restauração

```powershell
wsl --export Ubuntu-24.04 D:\backup\ubuntu.tar
wsl --import Ubuntu-restaurado D:\wsl\ubuntu D:\backup\ubuntu.tar
```
