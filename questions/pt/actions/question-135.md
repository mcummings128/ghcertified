---
question: "Você criou um fork de um repositório para aprimorar um fluxo de trabalho que utiliza um segredo para acessar uma aplicação de terceiros. Você dispara o fluxo de trabalho antes de editar seu código para obter um resultado inicial, mas descobre que o fluxo de trabalho falha. Por que isso ocorre?"
documentation: "https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/use-secrets?tool=webui#using-secrets-in-a-workflow"
---

- [x] Repositórios criados como fork não herdam segredos do repositório original  
> Como medida de segurança, (exceto o `GITHUB_TOKEN`) os segredos não são passados para o runner quando um fluxo de trabalho é acionado a partir de um repositório criado como fork. Isso resulta na falha do fluxo de trabalho se ele referenciar um segredo do repositório original.
- [ ] Ao herdar o segredo do repositório original, ocorreu um erro durante o fork que resultou em um segredo malformado ou inválido  
> Exceto pelo `GITHUB_TOKEN`, os segredos não são passados para o runner quando um fluxo de trabalho é acionado a partir de um repositório criado como fork. Assim, nenhuma malformação poderia ocorrer.
- [ ] O segredo herdado tinha um tamanho maior que 48 KB  
> Exceto pelo `GITHUB_TOKEN`, os segredos não são passados para o runner quando um fluxo de trabalho é acionado a partir de um repositório criado como fork. Assim, o tamanho não é um fator a ser considerado.
- [ ] Repositórios criados como fork herdam apenas segredos de repositório, então o segredo utilizado no fluxo de trabalho deve ser um segredo organizacional ou ambiental.  
> Exceto pelo `GITHUB_TOKEN`, os segredos não são passados para o runner quando um fluxo de trabalho é acionado a partir de um repositório criado como fork. Isso se aplica a todos os tipos de segredos (repositório, ambiente e organizacional).
