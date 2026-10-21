# Manual de OpenShift Dev Spaces

**Ambientes de desenvolvimento na nuvem, prontos em minutos e acessados pelo navegador.**
O Red Hat OpenShift Dev Spaces, baseado no projeto open source [Eclipse Che](https://eclipse.dev/che/),
cria um *workspace* (editor, ferramentas, runtimes e código) dentro do cluster OpenShift.

[Começar o onboarding →](onboarding/trilha.md){ .md-button .md-button--primary }
[Criar meu primeiro workspace](onboarding/primeiros-30-minutos.md){ .md-button }

```mermaid
flowchart TB
    dev([👩‍💻 Pessoa desenvolvedora · só precisa do navegador]):::pessoa
    dash[🧭 Dashboard do Dev Spaces]:::devspaces
    git[(🐙 Repositório Git com devfile.yaml)]:::git
    subgraph ws [Workspace · pod no projeto do usuário, dentro do OpenShift]
        direction LR
        ide[🖥️ VS Code ou IntelliJ]:::editor
        tools[🧰 Ferramentas · runtimes, CLIs, oc]:::editor
        code[(📂 Código)]:::dados
    end

    dev -- 1 · login OpenShift --> dash
    dash -- 2 · cria a partir do devfile --> ws
    git -- 3 · clone --> code
    dev -. 4 · edita no navegador .-> ide

    classDef pessoa fill:#e2e8f0,stroke:#64748b,color:#0f172a
    classDef devspaces fill:#fee2e2,stroke:#ef4444,color:#7f1d1d
    classDef editor fill:#dbeafe,stroke:#3b82f6,color:#1e3a8a
    classDef dados fill:#f3e8ff,stroke:#a855f7,color:#581c87
    classDef git fill:#dcfce7,stroke:#22c55e,color:#14532d
```

*Figura 1 · O dashboard cria o workspace a partir do `devfile.yaml` do repositório; a pessoa usa o editor no navegador.*

## Por que usar

<div class="grid cards" markdown>

-   ⚡ __Onboarding em minutos__

    ---

    Um link abre o ambiente pronto. Nada para instalar na máquina.

-   📄 __Ambiente como código__

    ---

    O `devfile.yaml` no repositório define ferramentas, comandos e portas. Todos usam o mesmo ambiente.

-   🔒 __Código dentro da rede__

    ---

    O código não sai do cluster. Login pelo OpenShift (OAuth, LDAP/AD), com RBAC e quotas.

-   🧩 __Editores conhecidos__

    ---

    VS Code (build open source) ou JetBrains IntelliJ IDEA, no navegador.

</div>

## Por onde começar

| Você é | Comece por |
|--------|-----------|
| Pessoa desenvolvedora | [Trilha de onboarding](onboarding/trilha.md) |
| Tech lead preparando um repositório | [Devfile](uso/devfile.md) |
| Admin da plataforma | [Instalação](administracao/instalacao.md) |

!!! tip "Sem cluster? Teste grátis"
    O [Developer Sandbox da Red Hat](https://developers.redhat.com/developer-sandbox) inclui o
    Dev Spaces e não tem custo.

**Referências:** [Página do produto](https://developers.redhat.com/products/openshift-dev-spaces) ·
[Documentação oficial](https://docs.redhat.com/en/documentation/red_hat_openshift_dev_spaces/latest)
