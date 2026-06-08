---
question: "Observe os valores na chave `runs-on`, como exibido na etapa do fluxo de trabalho abaixo. O que é verdadeiro em relação à execução da etapa?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-runners/self-hosted-runners/use-in-a-workflow#using-custom-labels-to-route-jobs"
---
```yaml
jobs:
    fire_emblem_deploy:
        name: "Implantar o aplicativo 'Fire Emblem'"
        runs-on: [self-hosted,nes,linux]
```

- [x] A etapa será executada em um runner self-hosted que tenha todos os rótulos aplicados.
- [ ] A etapa será executada em um runner self-hosted que tenha qualquer um dos rótulos aplicados.
> Os rótulos do runner são aplicados cumulativamente; um fluxo de trabalho não será executado em um runner que tenha apenas alguns dos rótulos. Todos eles são necessários.
- [ ] A etapa ainda poderá ser executada em runners hospedados pelo GitHub, já que eles podem ter rótulos personalizados aplicados.
> Os runners hospedados pelo GitHub não podem ter rótulos personalizados aplicados. Eles devem ser referenciados com os [rótulos predefinidos](https://docs.github.com/en/enterprise-cloud@latest/actions/how-tos/write-workflows/choose-where-workflows-run/choose-the-runner-for-a-job#standard-github-hosted-runners-for-public-repositories) que foram atribuídos a eles.
- [ ] A etapa será executada em um runner (self-hosted ou hospedado pelo GitHub, o que estiver disponível primeiro) com o nome `self-hosted,nes,linux`
> `runs-on` aponta para rótulos de runner, não nomes.
