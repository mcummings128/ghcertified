---
question: "W jaki sposób można zmienić okres przechowywania artefaktów generowanych przez określony workflow?"
documentation: "https://github.com/actions/upload-artifact#inputs"
---

- [x] Korzystając z wejścia `retention-days` w `actions/upload-artifact`
- [ ] Korzystając z wejścia `retention-days` w `actions/download-artifact`
> `actions/download-artifact` służy do pobierania artefaktów. W związku z tym nie ma wpływu na długość przechowywania przesłanego artefaktu. Dodatkowo, `retention-days` nie jest wejściem dla tego działania. Zobacz [dokumentację](https://github.com/actions/download-artifact#inputs) po więcej szczegółów.
- [ ] Przechodząc do ustawień Actions w repozytorium i edytując wartość ustawienia "Artifact and log retention" dla wymienionego workflow.
> Choć można edytować ustawienie ["Artifact and log retention"](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-repository) w repozytorium, ustawienie to dotyczy wszystkich workflow w repozytorium, a nie konkretnego workflow. To ustawienie nie wymienia poszczególnych workflow.
- [ ] Przechodząc do ustawień Actions organizacji i edytując wartość ustawienia "Artifact and log retention"
> Choć można edytować ustawienie ["Artifact and log retention"](https://docs.github.com/en/organizations/managing-organization-settings/configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-organization) w organizacji, ustawienie to dotyczy wszystkich workflow w danej organizacji, a nie konkretnego workflow.
