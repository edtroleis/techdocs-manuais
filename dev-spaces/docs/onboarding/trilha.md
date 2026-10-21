# Trilha de onboarding

!!! abstract "Em uma frase"
    Em **30 minutos** você abre o primeiro workspace; no **primeiro dia** trabalha num repositório
    do time; na **primeira semana** entrega um PR feito inteiramente no Dev Spaces.

```mermaid
flowchart TB
    subgraph m30 [⏱️ Primeiros 30 minutos]
        direction LR
        a1[Login no dashboard]:::etapa --> a2[Workspace de exemplo]:::etapa --> a3[Terminal e editor]:::etapa
    end
    subgraph d1 [📅 Primeiro dia]
        direction LR
        b1[Workspace do repo do time]:::etapa --> b2[Rodar e depurar]:::etapa --> b3[Git e tokens]:::etapa
    end
    subgraph s1 [🗓️ Primeira semana]
        direction LR
        c1[Entender o devfile]:::etapa --> c2[Melhorar o devfile]:::etapa --> c3[Primeiro PR 🎉]:::fim
    end
    m30 --> d1 --> s1

    classDef etapa fill:#dbeafe,stroke:#3b82f6,color:#1e3a8a
    classDef fim fill:#dcfce7,stroke:#22c55e,color:#14532d
```

*Figura 2 · A jornada de onboarding em três etapas, do primeiro login ao primeiro PR.*

| Etapa | Objetivo | Guia | Checklist |
|-------|----------|------|-----------|
| ⏱️ 30 minutos | Primeiro workspace aberto | [Primeiros 30 minutos](primeiros-30-minutos.md) | 4 itens |
| 📅 Dia 1 | Trabalhando no repositório do time | [Primeiro dia](primeiro-dia.md) | 6 itens |
| 🗓️ Semana 1 | Autonomia: PR entregue, devfile entendido | [Primeira semana](primeira-semana.md) | 5 itens |

## Antes de começar

- [ ] Você tem login no cluster OpenShift (o mesmo das outras ferramentas).
- [ ] Sabe a URL do Dev Spaces da organização, por exemplo `https://devspaces.apps.<cluster>`.
- [ ] Tem acesso de leitura ao repositório do time no Git.

!!! info "Quem ajuda"
    Dúvidas de uso: seu buddy de onboarding. Problemas na plataforma: `platform-team`.
    Veja também o [Onboarding de TI](http://localhost:3000/docs/default/component/onboarding-ti).
