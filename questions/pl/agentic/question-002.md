---
question: "Które polecenie GitHub CLI rozpoczyna nową sesję agenta chmurowego Copilot do autonomicznej pracy nad zadaniem?"
documentation: "https://docs.github.com/en/copilot/how-tos/use-copilot-agents/cloud-agent/create-a-pr"
---

- [x] `gh agent-task create`
> `gh agent-task create` (wymaga GitHub CLI v2.80.0+) rozpoczyna sesję agenta chmurowego, który może tworzyć branche i pull requests.
- [ ] `gh copilot agent start`
> To polecenie nie istnieje w GitHub CLI.
- [ ] `gh workflow run copilot-agent`
> To polecenie uruchomiłoby workflow GitHub Actions, a nie sesję agenta chmurowego Copilot.
- [ ] `gh issue assign --copilot`
> Można przypisać zadania Copilot przez API, ale to nie jest poprawna składnia polecenia CLI.
