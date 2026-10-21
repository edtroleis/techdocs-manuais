# Problemas comuns

??? question "O workspace fica em Starting e não abre"
    Veja os eventos e logs no dashboard (workspace → **Logs**). Causas comuns: imagem não
    encontrada, quota do projeto esgotada ou volume sem espaço.

??? question "Não consigo fazer push para o Git"
    Autorize o provedor em **User Preferences → Git Services** ou cadastre um token em
    **Personal Access Tokens**.

??? question "A aplicação roda, mas não abre no navegador"
    Confira o `endpoints` no devfile: `targetPort` igual à porta da aplicação e
    `exposure: public`. A aplicação deve escutar em `0.0.0.0`.

??? question "Meu workspace parou sozinho"
    É a parada por inatividade. O código está no volume; inicie de novo pelo dashboard.

??? question "Faltou memória (OOMKilled)"
    Aumente o `memoryLimit` do container no devfile, dentro da quota do projeto.
