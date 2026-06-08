---
question: "Poniższy przepływ pracy wywołuje wielokrotnego użytku przepływ pracy w jednym ze swoich zadań. Wielokrotnego użytku przepływ pracy ma zdefiniowane `permissions` na poziomie przepływu, jak pokazano poniżej. Jaki będzie wynik wywołania przepływu pracy wielokrotnego użytku?"
documentation: "https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows"
---

```yaml
# przepływ pracy wywołujący
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

# przepływ pracy wielokrotnego użytku (issue-creator.yml)
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
- [x] Wielokrotnego użytku przepływ pracy zwróci błąd, ponieważ zadanie, które go wywołało, ma tylko uprawnienia `contents: read`
> W tym scenariuszu wywołujący przepływ pracy zostanie uruchomiony, ale jego zadanie nie zostanie wykonane. Zamiast tego wygenerowany zostanie błąd, który informuje, że plik wywołującego przepływu pracy jest nieprawidłowy, ponieważ przepływ pracy wielokrotnego użytku wymaga `contents: write`, podczas gdy jest tylko dozwolone `contents: read`.
- [ ] Wielokrotnego użytku przepływ pracy utworzy zgłoszenie w repozytorium zatytułowane `"Issue Report"`
> To wystąpiłoby, gdyby zadanie `issue_creator` miało uprawnienia `contents:write`, które odziedziczyłby wielokrotnego użytku przepływ pracy.
- [ ] Wielokrotnego użytku przepływ pracy nie zostanie wywołany, ponieważ przepływy pracy wielokrotnego użytku muszą znajdować się w podfolderze `.github/workflows`
> Wszystkie przepływy pracy muszą być zlokalizowane w katalogu `.github/workflows`.
- [ ] Wywołujący i wielokrotnego użytku przepływ pracy nie zostaną wywołane, ponieważ `issues` nie jest dostępny jako wyzwalacz dla GitHub Actions. 
> `issues` jest standardowym zdarzeniem wyzwalającym, co pokazano w [dokumentacji](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#issues)
