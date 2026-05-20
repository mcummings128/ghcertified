---
question: "W jaki sposób można usuwać artefakty workflow?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-workflow-runs/remove-workflow-artifacts"
---

- [x] Korzystając z interfejsu użytkownika Github Actions, aby przejść do uruchomienia workflow i usuwać artefakty indywidualnie
- [x] Korzystając z interfejsu użytkownika Github Actions, aby usunąć uruchomienie workflow, które wygenerowało artefakty
> Usunięcie uruchomienia workflow powoduje również usunięcie powiązanych z nim artefaktów.
- [x] Korzystając z odpowiedniego endpointa GitHub API
> GitHub API zawiera endpoint "Delete an artifact". Zobacz [dokumentację](https://docs.github.com/en/rest/actions/artifacts?apiVersion=2026-03-10#delete-an-artifact) po więcej szczegółów.
- [ ] Korzystając z akcji `actions/delete-artifact` we workflow
- [ ] Poprzez zdalne połączenie z hostowanymi lokalnie runnerami za pomocą SSH, przejście do katalogu `.github/artifacts` i usunięcie wybranych artefaktów
> Artefakty są zazwyczaj przechowywane w infrastrukturze GitHub, a nie na runnerach.
- [ ] Poprzez ustawienie okresu przechowywania artefaktu na 0 dni
> Okresy przechowywania artefaktów nie mogą być ustawione na 0 dni. Zobacz [dokumentację](https://docs.github.com/en/organizations/managing-organization-settings/configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-organization) po więcej informacji.
