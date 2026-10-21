# Configuração

A configuração fica no recurso `CheCluster`:

```bash
oc edit checluster/devspaces -n openshift-devspaces
```

| Tema | Onde no `CheCluster` | Recomendação |
|------|----------------------|--------------|
| Inatividade | `spec.devEnvironments.secondsOfInactivityBeforeIdling` | 30 min |
| Tempo máximo rodando | `spec.devEnvironments.secondsOfRunBeforeIdling` | Por política |
| Armazenamento | `spec.devEnvironments.storage` | `per-user` |
| Workspaces simultâneos | `spec.devEnvironments.maxNumberOfRunningWorkspacesPerUser` | 1–2 |
| Proxy e CAs | `spec.components.cheServer.proxy` + ConfigMap de certificados | Conforme a rede |
| Integração Git (OAuth) | Secret de OAuth por provedor | GitHub/GitLab da organização |

!!! warning "Quotas"
    Combine com `ResourceQuota` e `LimitRange` nos projetos dos usuários para evitar que poucos
    workspaces consumam o cluster.
