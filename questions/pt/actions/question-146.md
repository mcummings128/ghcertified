---
question: "Quais afirmações são verdadeiras sobre `github.ref` quando o workflow é acionado por um evento `pull_request`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] Em pull requests que não foram mesclados, `github.ref` refere-se à referência completa do branch/tag de mesclagem do pull request 
> Para mais informações sobre referências, veja a documentação oficial do [Git](https://git-scm.com/book/en/Git-Internals-Git-References).
- [x] Em pull requests que foram mesclados, `github.ref` refere-se à referência completa do branch que foi mesclado.
- [ ] Em pull requests (independentemente do status de mesclagem), `github.ref` refere-se ao número do pull request 
> Para o evento `pull_request`, o valor de `github.ref` varia dependendo de o pull request ter sido ou não mesclado. Este valor sempre será uma referência, não o número do pull request.
- [ ] Em pull requests (independentemente do status de mesclagem), `github.ref` é o SHA do último commit de mesclagem no branch `GITHUB_REF`.
> `github.sha` é o que aponta para o último SHA no branch de mesclagem (ex. `refs/pull/PULL_REQUEST_NUMBER/merge`). Consulte a [documentação de eventos](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request) para mais detalhes (procure por `GITHUB_SHA`).
- [ ] Em pull requests que não foram mesclados, `github.ref` é a referência completa do título do pull request. 
> Referências não são formadas a partir de títulos dos pull requests. `github.event.pull_request.title` é o que contém o título do pull request. Consulte a [documentação](https://docs.github.com/en/webhooks/webhook-events-and-payloads#pull_request) para mais detalhes.
- [ ] Em pull requests que foram mesclados, `github.ref` é o tipo de referência completa que acionou a execução do workflow. O valor será `branch`, `tag` ou `null` (se a referência não estiver completa).
> `github.ref_type` é o valor do tipo de referência que acionou a execução do workflow. Ele pode conter apenas `branch` ou `tag`; `null` não é um valor válido. Consulte o link da documentação nesta pergunta para mais detalhes.
