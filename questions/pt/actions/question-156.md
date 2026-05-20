---
question: "De que maneiras você pode excluir artefatos de workflows?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-workflow-runs/remove-workflow-artifacts"
---

- [x] Usando a interface do GitHub Actions para navegar até uma execução de workflow e excluir os artefatos individualmente
- [x] Usando a interface do GitHub Actions para excluir a execução do workflow que gerou os artefatos
> Excluir uma execução de workflow também exclui os artefatos associados à execução.
- [x] Usando um endpoint específico da API do GitHub
> A API do GitHub possui um endpoint "Excluir um artefato". Consulte a [documentação](https://docs.github.com/en/rest/actions/artifacts?apiVersion=2026-03-10#delete-an-artifact) para mais detalhes.
- [ ] Usando a action `actions/delete-artifact` em um workflow
- [ ] Acessando remotamente runners hospedados por você via SSH, navegando até o diretório `.github/artifacts` e excluindo os artefatos selecionados
> Os artefatos geralmente são armazenados usando a infraestrutura do GitHub, não runners hospedados por você.
- [ ] Configurando o período de retenção de artefatos para 0 dias
> Os períodos de retenção de artefatos não podem ser configurados para 0 dias. Consulte a [documentação](https://docs.github.com/en/organizations/managing-organization-settings/configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-organization) para mais informações.
