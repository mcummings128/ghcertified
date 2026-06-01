---
question: "Quais das opções a seguir são verdadeiras ao comparar os eventos pull_request e pull_request_target?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request"
---

- [x] O evento `pull_request` é executado no contexto do commit de mesclagem, enquanto o `pull_request_target` é executado no contexto da branch padrão do repositório base.  
> Para mais informações sobre commits de mesclagem, veja a [documentação](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges) do GitHub.  
- [x] Os workflows não serão executados na atividade `pull_request` se houver um conflito de mesclagem.  
- [x] Ambos os eventos `pull_request` e `pull_request_target` têm tipos de atividades padrão `opened`, `synchronize` e `reopened`.  
- [ ] `pull_request` deve ser usado com cautela, já que PRs de forks permitirão que o workflow acesse todos os segredos dentro do repositório devido a estar associado à branch padrão.  
> Isto é verdadeiro para `pull_request_target`; `pull_request` não está associado à branch padrão e, portanto, quando acionado por PRs vindos de forks, o workflow terá acesso limitado aos segredos. Veja a seção "pull_request_target" na documentação acima para mais informações.  
- [ ] Os workflows não serão executados na atividade `pull_request_target` se houver um conflito de mesclagem.  
- [ ] O evento `pull_request_target` deve ser usado quando você desejar executar o código contido nos arquivos modificados de um PR, para realizar atividades como verificações de CI ou execução de suítes de testes.  
> `pull_request_target` é executado no contexto da branch padrão do repositório, o que pode levar a códigos não confiáveis sendo carregados e executados por atividades como verificações de CI ou suítes de testes. Veja a [documentação](https://docs.github.com/en/enterprise-cloud@latest/actions/reference/security/secure-use#mitigating-the-risks-of-untrusted-code-checkout) para mais informações.  
