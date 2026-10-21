# Validação

```powershell
wsl --status
wsl -l -v          # VERSION deve ser 2
```

Dentro da distribuição:

```bash
uname -r                     # kernel com "microsoft-standard-WSL2"
systemctl is-system-running  # running/degraded = systemd ativo
curl -sI https://github.com | head -1
df -h ~                      # espaço em disco
```

- [ ] Distribuição em WSL 2
- [ ] systemd ativo
- [ ] Acesso à internet (e ao proxy corporativo, se houver)
- [ ] Código em `~/code`
