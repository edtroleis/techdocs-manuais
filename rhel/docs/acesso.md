# Acesso

## Registro da assinatura

```bash
sudo subscription-manager register --username <usuario>
sudo subscription-manager status
```

## Usuários

```bash
sudo useradd -m -G wheel maria
sudo passwd maria
```

O grupo `wheel` concede `sudo`. Não use o usuário `root` no dia a dia.

## SSH com chave

```bash
ssh-keygen -t ed25519 -C "maria@estacao"
ssh-copy-id maria@servidor
```

Em `/etc/ssh/sshd_config.d/10-hardening.conf`:

```text
PermitRootLogin no
PasswordAuthentication no
```

```bash
sudo systemctl reload sshd
```
