# Segurança

## Atualizações

```bash
sudo dnf updateinfo list --security
sudo dnf update --security -y
```

## SELinux

Mantenha em **enforcing**:

```bash
getenforce
sudo ausearch -m avc -ts recent   # negações recentes
```

Corrija o contexto em vez de desabilitar o SELinux:

```bash
sudo semanage fcontext -a -t httpd_sys_content_t "/srv/site(/.*)?"
sudo restorecon -Rv /srv/site
```

## Firewall

```bash
sudo firewall-cmd --list-all
sudo firewall-cmd --permanent --add-service=https
sudo firewall-cmd --reload
```

- [ ] Atualizações de segurança aplicadas
- [ ] SELinux em enforcing
- [ ] Firewall ativo, só com os serviços necessários
- [ ] SSH sem root e sem senha
