# Problemas comuns

??? question "Cannot connect to Podman"
    A Podman machine está parada: `podman machine start`.

??? question "Porta já em uso"
    Outro processo usa a porta: mude o mapeamento (`-p 8081:80`).

??? question "Erro de certificado ao fazer pull (proxy corporativo)"
    Importe o certificado da CA corporativa na Podman machine (ou na distribuição WSL).

??? question "Ferramenta exige Docker"
    Exponha o socket do Podman e defina `DOCKER_HOST`; o Podman Desktop oferece a opção de
    compatibilidade com Docker.
