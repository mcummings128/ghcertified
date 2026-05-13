---
question: "Qual afirmação é verdadeira sobre `github.ref` quando o fluxo de trabalho é acionado por um evento de push?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] Em eventos de push, `github.ref` é a referência completamente formada do branch ou tag que foi enviado. 
> Para mais informações sobre referências, veja a [documentação oficial do Git](https://git-scm.com/book/en/Git-Internals-Git-References).
- [ ] Em eventos de push, `github.ref` é a mensagem do commit que acionou o fluxo de trabalho.
> `github.event.head_commit.message` é onde está a mensagem do último commit. Veja a [documentação](https://docs.github.com/en/webhooks/webhook-events-and-payloads#push) para mais detalhes.
- [ ] Em eventos de push, `github.ref` é o SHA do commit que acionou o fluxo de trabalho.
> `github.sha` é o que aponta para o SHA do commit. Consulte a [documentação de eventos](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows) e o link do documento nesta pergunta para mais detalhes.
- [ ] Em eventos de push, `github.ref` é a descrição do commit que acionou o fluxo de trabalho.
- [ ] Em eventos de push, `github.ref` é o tipo de referência completamente formada que acionou a execução do fluxo de trabalho. O valor será `branch`, `tag` ou `null` (se a referência não estiver completamente formada).
> `github.ref_type` é o valor do tipo de referência que acionou a execução do fluxo de trabalho. Ele pode conter apenas `branch` ou `tag`; `null` não é um valor válido. Veja o link do documento nesta pergunta para mais detalhes.
