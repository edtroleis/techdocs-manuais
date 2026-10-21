# Instalação

!!! note "Para admins da plataforma"
    Esta página é para quem administra o cluster. Pessoas desenvolvedoras podem pular.

O Dev Spaces está incluído na assinatura do OpenShift e é instalado por **Operator**. Ele depende
do **Dev Workspace Operator**, que é instalado junto. Referência:
[Administration guide · Installing Dev Spaces](https://docs.redhat.com/en/documentation/red_hat_openshift_dev_spaces/latest/html/administration_guide/installing-devspaces).

=== "🖱️ Console web (OperatorHub)"

    1. **Operators → OperatorHub** → procure *Red Hat OpenShift Dev Spaces* → **Install**.
    2. Crie o projeto `openshift-devspaces`.
    3. **Installed Operators → Red Hat OpenShift Dev Spaces → Create instance** (CheCluster),
       no namespace `openshift-devspaces`.
    4. Aguarde a URL do Dev Spaces aparecer no status da instância.

=== "⌨️ CLI (dsc)"

    Com uma sessão `oc` de administrador e o CLI [`dsc`](https://developers.redhat.com/products/openshift-dev-spaces/download):

    ```bash
    dsc server:deploy --platform openshift
    dsc server:status
    dsc dashboard:open
    ```

## Verificação

- [ ] Instância `CheCluster` sem mensagens de erro no status
- [ ] URL do Dev Spaces disponível e acessível
- [ ] Um workspace de exemplo inicia com sucesso
