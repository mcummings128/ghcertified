---
question: "Twoja organizacja chce skrócić okres przechowywania zapisanych artefaktów z powodu obaw dotyczących przestrzeni dyskowej. W jaki sposób można to zrobić na poziomie organizacyjnym?"
documentation: "https://docs.github.com/en/organizations/managing-organization-settings/configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-organization"
---

- [x] Przechodząc do ustawień Actions organizacji i edytując wartość ustawienia „Artifact and log retention”
- [ ] Korzystając z runnerów hostowanych lokalnie, tworząc plik `.github/retention-policy.yml` i określając wartość klucza `artifact-retention-period`
> Dostosowanie okresów przechowywania artefaktów nie jest ograniczone do runnerów hostowanych lokalnie.  
- [ ] Nie można tego zrobić na poziomie organizacyjnym. Wszystkie workflowy wykorzystujące `actions/upload-artifact` muszą używać wymaganego argumentu `retention-days`.
> Chociaż argument `retention-days` może być użyty do dostosowania okresu przechowywania dla poszczególnych artefaktów tworzonych przez workflow, nie jest to odpowiednie w przypadku próby zastosowania ogólnej polityki na poziomie organizacyjnym. Co więcej, argument `retention-days` jest [opcjonalny, a nie wymagany](https://github.com/actions/upload-artifact#inputs).
- [ ] Nie można tego zrobić: artefakty są zawsze przechowywane przez 90 dni we wszystkich systemach implementujących Github Actions.
> Domyślny okres przechowywania artefaktów wynosi 90 dni. Możliwe jest jednak zmiana tej wartości we wszystkich systemach implementujących Github Actions.
