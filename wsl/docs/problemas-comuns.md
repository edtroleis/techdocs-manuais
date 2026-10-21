# Problemas comuns

??? question "Erro 0x80370102 ao iniciar"
    A virtualização está desabilitada na BIOS/UEFI, ou o recurso
    *Plataforma de Máquina Virtual* não está habilitado.

??? question "Sem internet dentro do WSL (VPN)"
    Use `networkingMode=mirrored` no `.wslconfig` e reinicie com `wsl --shutdown`.

??? question "Disco do WSL ocupando muito espaço"
    Habilite `sparseVhd=true` ou compacte o VHDX com a distribuição desligada.

??? question "Relógio dessincronizado após suspender"
    `sudo hwclock -s` ou reinicie o WSL com `wsl --shutdown`.
