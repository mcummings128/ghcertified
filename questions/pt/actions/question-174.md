---
question: "O seguinte workflow chama um workflow reutilizável em um de seus jobs. O workflow reutilizável possui `permissions` definidas no nível do workflow, conforme mostrado abaixo. Qual será o resultado de chamar o workflow reutilizável?"
documentation: "https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows"
---

```yaml
# workflow de chamado
on:
    issues:
        types: [opened]
    
    permissions:
        contents: write

    jobs:
        issue_creator:
            permissions:
                contents: read
            uses: ./.github/workflows/issue-creator.yml

# workflow reutilizável (issue-creator.yml)
on:
    workflow_call:

    permissions:
        contents: write

    jobs:
        create_issue:
            runs-on: ubuntu-latest
            steps: 
                env: GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}    
                - run: gh issue create --title "Issue report" --body "Hello!" --repo $GITHUB_REPOSITORY

```
- [x] O workflow reutilizável retornará um erro, já que o job que o chamou tem apenas permissões de `contents:read`
> Nesse cenário, o workflow de chamada é acionado, mas seu job não será executado. Em vez disso, será gerado um erro indicando que o arquivo do workflow de chamada não é válido, pois o workflow reutilizável está solicitando `contents:write`, mas apenas `contents:read` está autorizado.
- [ ] O workflow reutilizável criará uma issue no repositório intitulada `"Issue Report"`
> Isso aconteceria se o job `issue_creator` tivesse permissões de `contents:write`, que seriam herdadas pelo workflow reutilizável.
- [ ] O workflow reutilizável não será chamado, pois workflows reutilizáveis devem estar em uma subpasta de `.github/workflows`
> Todos os workflows devem estar localizados no diretório `.github/workflows`.
- [ ] Tanto o workflow de chamada quanto o reutilizável não serão acionados, pois `issues` não é um gatilho disponível para o GitHub Actions.
> `issues` é um evento padrão, conforme visto na [documentação](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#issues).
