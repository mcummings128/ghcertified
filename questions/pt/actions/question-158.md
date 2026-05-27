---
question: "Petra está criando um workflow cujo único trabalho é nomeado `post-merge`. Como ela pode configurar o trabalho para ser acionado após uma pull request ter sido mesclada?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#running-your-pull_request-workflow-when-a-pull-request-merges"
---

- [x] Especificar o tipo de atividade `pull_request` como `closed`, e usar uma condicional no nível do trabalho para verificar se `github.event.pull_request.merged` é verdadeiro
```yaml
on:
    pull_request:
        types: [closed]

jobs:
    post-merge:
        if: github.event.pull_request.merged == true
``` 
> Para acionar um trabalho de workflow quando uma pull request é mesclada, você deve especificar tanto o tipo de atividade da pull request em `on:` quanto definir uma condicional no nível do trabalho.
- [ ] Especificar o tipo de atividade `pull_request` como `merged`, e usar uma condicional no nível do trabalho para verificar se `github.event.pull_request.merged` é verdadeiro
```yaml
on:
    pull_request:
        types: [merged]
jobs:
    post-merge:
        if: github.event.pull_request.merged == true
``` 
> O evento `pull_request` não possui um tipo de atividade `merged`. Consulte a seção "pull_request" da documentação vinculada para ver os tipos de atividade válidos para `pull_request`.
- [ ] Especificar o tipo de atividade `pull_request` como `merged` (sem necessidade de uma condicional no nível do trabalho)
```yaml
on:
    pull_request:
        types: [merged]
jobs:
    post-merge:
``` 
> O evento `pull_request` não possui um tipo de atividade `merged`.
- [ ] Especificar o tipo de atividade `pull_request` como `closed` (sem necessidade de uma condicional no nível do trabalho)
```yaml
on:
    pull_request:
        types: [closed]
jobs:
    post-merge:
``` 
> Pull requests podem ser fechadas sem serem mescladas. Se você não usar uma condicional correspondente no nível do trabalho que verifica se a PR foi mesclada, então o trabalho será acionado sempre que uma PR for fechada, não apenas quando a mesclagem ocorrer.
- [ ] Especificar o tipo de atividade `pull_request` como `closed` e usar uma condicional no nível do trabalho para verificar se `github.ref` é igual ao branch de mesclagem da pull request.
```yaml
on:
    pull_request:
        types: [closed]
jobs:
    post-merge: 
        if: ${{ github.ref == github.event.pull_request.base.ref }}
``` 
> Após uma pull request ter sido mesclada, `github.ref` será o *ref totalmente formado* do branch de mesclagem (ex. `refs/heads/main`), e não simplesmente o branch de mesclagem (ex. `main`).
