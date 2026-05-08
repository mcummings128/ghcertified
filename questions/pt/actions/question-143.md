---
question: "Sua organização deseja reduzir o período de retenção para artefatos armazenados, citando preocupações com armazenamento. Como isso pode ser feito no nível organizacional?"
documentation: "https://docs.github.com/en/organizations/managing-organization-settings/configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-organization"
---

- [x] Navegando para as configurações de Actions da organização e editando o valor da configuração "Artifact and log retention"
- [ ] Usando runners auto-hospedados, criando um arquivo `.github/retention-policy.yml` e especificando o valor da chave `artifact-retention-period`
> Personalizar períodos de retenção de artefatos não se limita a runners auto-hospedados.  
- [ ] Isso não pode ser feito no nível organizacional. Todos os workflows que utilizam `actions/upload-artifact` devem usar o campo obrigatório `retention-days`.
> Embora o campo `retention-days` possa ser usado para personalizar o período de retenção para artefatos individuais criados por um workflow, isso é inadequado se a intenção for aplicar uma política geral no nível organizacional. Além disso, o campo `retention-days` é [opcional, não obrigatório](https://github.com/actions/upload-artifact#inputs).
- [ ] Isso não pode ser feito: os artefatos são estritamente armazenados por 90 dias em todos os sistemas que implementam o Github Actions.
> O período padrão de retenção para artefatos é de 90 dias. É possível alterar esse valor em todos os sistemas que implementam o Github Actions. 
