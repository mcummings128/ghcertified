---
question: "Quais afirmações são verdadeiras em relação ao `github.ref` quando o workflow é acionado por um evento de `pull_request`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] Em pull requests que não foram mesclados, `github.ref` refere-se ao ref totalmente formado do branch/tag de mesclagem do pull request. 
> Por exemplo, se o número do pull request (aberto) fosse #123, `github.ref` seria `refs/pull/123/merge`. Para mais informações sobre refs, consulte a documentação oficial do [Git](https://git-scm.com/book/en/Git-Internals-Git-References).
- [x] Em pull requests que foram mesclados, `github.ref` refere-se ao ref totalmente formado do branch que foi mesclado. 
> Por exemplo, se você estivesse mesclando algo no branch `main`, `github.ref` seria `ref/heads/main` após o pull request ser mesclado.
- [ ] Em pull requests (independentemente do status de mesclagem), `github.ref` refere-se ao número do pull request. 
> Para o evento `pull_request`, o valor de `github.ref` varia dependendo se o pull request foi mesclado ou não. Este valor será sempre um ref, não o número do pull request.
- [ ] Em pull requests (independentemente do status de mesclagem), `github.ref` é o SHA do último commit de mesclagem do branch `GITHUB_REF`. 
> `github.sha` é o que aponta para o último SHA no branch de mesclagem (ex. `refs/pull/PULL_REQUEST_NUMBER/merge`). Consulte a [documentação de eventos](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request) para mais detalhes (busque por `GITHUB_SHA`).
- [ ] Em pull requests que não foram mesclados, `github.ref` é o ref totalmente formado do título do pull request. 
> Os refs não são formados a partir de títulos de pull request. `github.event.pull_request.title` é o que contém o título do pull request. Veja a [documentação](https://docs.github.com/en/webhooks/webhook-events-and-payloads#pull_request) para mais detalhes.
- [ ] Em pull requests que foram mesclados, `github.ref` é o tipo de ref totalmente formado que acionou a execução do workflow. O valor será `branch`, `tag` ou `null` (se o ref não foi totalmente formado). 
> `github.ref_type` é o valor do tipo de ref que acionou a execução do workflow. Ele pode conter apenas `branch` ou `tag`; `null` não é um valor válido. Consulte o link da documentação nesta pergunta para mais detalhes.
