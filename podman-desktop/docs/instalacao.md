# Instalação

## Windows

```powershell
winget install RedHat.Podman-Desktop
```

Ou instale pelo catálogo de software corporativo. Ao abrir, o Podman Desktop oferece instalar
o Podman CLI. Aceite.

## Linux

```bash
# Fedora / RHEL
sudo dnf install -y podman
# Ubuntu
sudo apt install -y podman
# Podman Desktop (Flatpak)
flatpak install flathub io.podman_desktop.PodmanDesktop
```

## Verificação

```bash
podman --version
podman info --format '{{.Host.OS}} {{.Version.Version}}'
```
