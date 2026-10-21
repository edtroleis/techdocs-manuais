# Editores

| Editor | Como escolher | Observação |
|--------|---------------|------------|
| VS Code (open source) | Padrão | Extensões do [Open VSX](https://open-vsx.org/) |
| JetBrains IntelliJ IDEA | Dashboard → **Create Workspace** → **Choose an editor** | Também pode ser fixado no repositório |

## Extensões recomendadas

Crie `.vscode/extensions.json` no repositório para sugerir extensões a todos do time:

```json
{
  "recommendations": [
    "ms-python.python",
    "redhat.vscode-yaml",
    "redhat.vscode-openshift-connector"
  ]
}
```

## Editor fixo no repositório

`.che/che-editor.yaml` define o editor padrão para quem abrir o repositório:

```yaml
id: che-incubator/che-code/latest
```
