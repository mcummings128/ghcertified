---
question: "Qual comando do GitHub CLI inicia uma nova sessão de agente em nuvem do Copilot para trabalhar em uma tarefa de forma autônoma?"
documentation: "https://docs.github.com/en/copilot/how-tos/use-copilot-agents/cloud-agent/create-a-pr"
---

- [x] `gh agent-task create`
> `gh agent-task create` (requer o GitHub CLI v2.80.0+) inicia uma sessão de agente em nuvem que pode criar branches e pull requests.
- [ ] `gh copilot agent start`
> Este comando não existe no GitHub CLI.
- [ ] `gh workflow run copilot-agent`
> Isso executaria um workflow do GitHub Actions, não uma sessão de agente em nuvem do Copilot.
- [ ] `gh issue assign --copilot`
> Embora você possa atribuir issues ao Copilot via API, esta não é a sintaxe correta do comando CLI.
