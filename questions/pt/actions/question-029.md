---
question: "Seu fluxo de trabalho de análise de Pull Request utiliza várias ferramentas de análise de código e leva cerca de 20 minutos para ser concluído totalmente. Ele é acionado pelo evento `pull_request` com o filtro `branches` configurado para `master`. Portanto, se um desenvolvedor enviar vários commits dentro de poucos minutos, múltiplos fluxos de trabalho serão executados em paralelo. Como você pode parar todas as execuções de fluxos anteriores e executar apenas aquele com as alterações mais recentes?"
documentation: "https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#example-using-concurrency-to-cancel-any-in-progress-job-or-run"
---

- [x] Usar concurrency com cancel-in-progress
```yaml
concurrency:
  group: ${{ github.workflow }}-${{ github.ref }}
  cancel-in-progress: true
```
- [ ] Usar concurrency
```yaml
concurrency:
  group: ${{ github.ref }}
```
> Isso enfileiraria execuções nesse github ref. Não cancelará execuções anteriores

- [ ] Usar o filtro de tipos de atividade
```yaml
on:
  pull_request:
    branches:
      - master
    types: [latest]
```
> Não existe nenhum tipo de atividade como `latest` para o evento pull_request
- [ ] Usar a flag cancel-in-progress para o evento `pull_request`
```yaml
on:
  pull_request:
    branches:
      - master
    cancel-in-progress: true
```
> `cancel-in-progress` só pode ser usado dentro de um bloco `concurrency`. Não é uma chave válida para `pull_request`.
