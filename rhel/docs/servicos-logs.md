# Serviços e logs

```bash
systemctl status sshd
sudo systemctl enable --now podman.socket
systemctl list-units --failed
```

## Logs

```bash
journalctl -u sshd --since "1 hour ago"
journalctl -p err -b        # erros desde o último boot
journalctl -f               # acompanhar em tempo real
```

## Containers como serviço (Quadlet)

`~/.config/containers/systemd/web.container`:

```ini
[Container]
Image=docker.io/library/nginx:alpine
PublishPort=8080:80

[Install]
WantedBy=default.target
```

```bash
systemctl --user daemon-reload
systemctl --user start web
```
