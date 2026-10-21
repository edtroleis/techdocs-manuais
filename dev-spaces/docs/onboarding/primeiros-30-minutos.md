# Primeiros 30 minutos

## 1. Entre no dashboard

Abra a URL do Dev Spaces e faça login com sua conta do OpenShift. Na primeira vez, autorize o
acesso solicitado pelo OAuth.

## 2. Crie um workspace de exemplo

Em **Create Workspace**, escolha um dos *samples*, por exemplo **Python** ou **Node.js**. Em
cerca de um minuto o editor abre no navegador.

## 3. Explore

| Faça | Onde |
|------|------|
| Abra um terminal | Menu **Terminal → New Terminal** |
| Rode o comando do devfile | Paleta de comandos (`F1`) → **Tasks: Run Task** → **devfile** |
| Abra a aplicação | Notificação de porta aberta → **Open in New Tab** |
| Pare o workspace | Dashboard → **Workspaces** → ⋮ → **Stop** |

```bash
# no terminal do workspace
whoami
oc whoami          # já autenticado no cluster
python --version   # ou node --version
```

## Checklist

- [ ] Login no dashboard feito
- [ ] Workspace de exemplo aberto
- [ ] Comando do devfile executado e aplicação aberta
- [ ] Workspace parado ao final

!!! tip "Workspace parado não perde nada"
    Código e alterações ficam no volume persistente. Ao iniciar de novo, tudo está lá.
