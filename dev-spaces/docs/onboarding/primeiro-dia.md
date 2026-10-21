# Primeiro dia

## Abra o repositório do time

Monte a URL do workspace a partir do repositório (a chamada *factory URL*):

```text
https://devspaces.apps.<cluster>/#https://github.com/<org>/<repo>
```

Se o repositório tem um `devfile.yaml` na raiz, o Dev Spaces usa as ferramentas definidas nele.
Se não tem, cria um workspace genérico com a imagem universal (UDI).

!!! tip "Botão no README"
    Adicione um link no README do repositório. Quem chegar ao time abre o ambiente com um clique.

    ```markdown
    [![Abrir no Dev Spaces](https://www.eclipse.org/che/contribute.svg)](https://devspaces.apps.<cluster>/#https://github.com/<org>/<repo>)
    ```

## Configure o Git

No dashboard, em **User Preferences**:

| Aba | O que configurar |
|-----|------------------|
| Git Services | Autorize o GitHub/GitLab (OAuth) para clonar e fazer push |
| Personal Access Tokens | Alternativa ao OAuth |
| SSH Keys | Se o time usa SSH |
| Gitconfig | `user.name` e `user.email` |

## Rode e depure

```bash
# exemplos; o devfile do time define os comandos certos
make run
make test
```

Use a aba **Run and Debug** do editor; portas expostas aparecem como notificação.

## Checklist

- [ ] Workspace do repositório do time aberto pela factory URL
- [ ] Git autorizado e `gitconfig` preenchido
- [ ] Aplicação rodando no workspace
- [ ] Testes executados
- [ ] Um breakpoint funcionando no debugger
- [ ] Workspace parado ao fim do dia
