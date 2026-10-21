# Devfile

O `devfile.yaml` na raiz do repositório define o ambiente: **componentes** (containers e volumes),
**comandos** e **endpoints** (portas). Especificação: [devfile.io](https://devfile.io/).

## Exemplo comentado

```yaml
schemaVersion: 2.2.0
metadata:
  name: demo-service
components:
  - name: tools
    container:
      # imagem universal do Dev Spaces (UDI); use a tag da versão instalada no cluster
      image: registry.redhat.io/devspaces/udi-rhel9:<versão>
      memoryLimit: 2Gi
      cpuLimit: '1'
      mountSources: true
      endpoints:
        - name: api
          targetPort: 8080
          exposure: public
          protocol: https
  - name: pip-cache
    volume:
      size: 1Gi
commands:
  - id: install
    exec:
      component: tools
      commandLine: pip install -r app/requirements.txt
      workingDir: ${PROJECT_SOURCE}
  - id: run
    exec:
      component: tools
      commandLine: uvicorn app.main:app --host 0.0.0.0 --port 8080
      workingDir: ${PROJECT_SOURCE}
      group:
        kind: run
        isDefault: true
events:
  postStart:
    - install
```

| Bloco | Para quê |
|-------|----------|
| `components.container` | Imagem com as ferramentas, limites de recursos e portas |
| `components.volume` | Cache persistente (dependências, builds) |
| `commands` | Tarefas que aparecem no editor (**Tasks: Run Task → devfile**) |
| `events.postStart` | Comandos executados ao iniciar o workspace |

!!! tip "Limites de recursos"
    Defina `memoryLimit` e `cpuLimit`. Sem eles, o workspace usa os padrões do cluster e pode
    faltar memória ou sobrar desperdício.
