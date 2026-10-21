# Boas práticas

<div class="grid cards" markdown>

-   🛑 __Pare o que não usa__

    ---

    Workspace parado não consome CPU nem memória. Pare ao fim do dia.

-   📄 __Devfile no repositório__

    ---

    Ambiente versionado junto do código; mudanças passam por PR.

-   📏 __Limites definidos__

    ---

    `memoryLimit` e `cpuLimit` em todo container do devfile.

-   💾 __Commit frequente__

    ---

    O volume persiste, mas o repositório é a fonte da verdade.

-   🔐 __Nada de segredos no devfile__

    ---

    Use secrets do OpenShift montados no workspace.

-   🧹 __Apague os antigos__

    ---

    Workspaces que você não usa mais ocupam volume.

</div>
