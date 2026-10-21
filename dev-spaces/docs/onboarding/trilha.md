# Trilha de onboarding

!!! abstract "Em uma frase"
    Em **30 minutos** você abre o primeiro workspace; no **primeiro dia** trabalha num repositório
    do time; na **primeira semana** entrega um PR feito inteiramente no Dev Spaces.

```mermaid
journey
    title Onboarding no OpenShift Dev Spaces
    section Primeiros 30 minutos
      Login no dashboard: 5: Dev
      Workspace de exemplo: 5: Dev
      Terminal e editor: 4: Dev
    section Primeiro dia
      Workspace do repo do time: 4: Dev
      Rodar e depurar a aplicação: 3: Dev, Buddy
      Configurar Git e tokens: 3: Dev
    section Primeira semana
      Ajustar o devfile: 3: Dev, Tech lead
      Primeiro PR pelo Dev Spaces: 5: Dev
```

*Figura 2 · A jornada de onboarding. A nota de 1 a 5 indica o esforço esperado em cada etapa.*

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
