---
question: "Petra buduje workflow, którego jedynym zadaniem jest zadanie o nazwie `post-merge`. Jak może skonfigurować zadanie, aby wyzwalało się po scaleniu pull requesta?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#running-your-pull_request-workflow-when-a-pull-request-merges"
---

- [x] Określ typ aktywności `pull_request` jako `closed` i użyj warunku na poziomie zadania, aby sprawdzić, czy `github.event.pull_request.merged` jest prawdą
```yaml
on:
    pull_request:
        types: [closed]

jobs:
    post-merge:
        if: github.event.pull_request.merged == true
``` 
> Aby wyzwolić zadanie workflow po scaleniu pull requesta, musisz określić zarówno typ aktywności pull requesta w `on:`, jak i ustawić warunek na poziomie zadania.
- [ ] Określ typ aktywności `pull_request` jako `merged` i użyj warunku na poziomie zadania, aby sprawdzić, czy `github.event.pull_request.merged` jest prawdą
```yaml
on:
    pull_request:
        types: [merged]
jobs:
    post-merge:
        if: github.event.pull_request.merged == true
``` 
> Zdarzenie `pull_request` nie ma typu aktywności `merged`. Zapoznaj się z sekcją "pull_request" w podlinkowanej dokumentacji, aby zobaczyć prawidłowe typy aktywności dla `pull_request`.
- [ ] Określ typ aktywności `pull_request` jako `merged` (nie ma potrzeby używania warunku na poziomie zadania)
```yaml
on:
    pull_request:
        types: [merged]
jobs:
    post-merge:
``` 
> Zdarzenie `pull_request` nie ma typu aktywności `merged`.
- [ ] Określ typ aktywności `pull_request` jako `closed` (nie ma potrzeby używania warunku na poziomie zadania)
```yaml
on:
    pull_request:
        types: [closed]
jobs:
    post-merge:
``` 
> Pull requesty mogą zostać zamknięte bez ich scalania. Jeśli nie użyjesz odpowiedniego warunku na poziomie zadania, który sprawdza, czy PR został scalony, zadanie uruchomi się za każdym razem, gdy PR zostanie zamknięty, a nie tylko po scaleniu.
- [ ] Określ typ aktywności `pull_request` jako `closed` i użyj warunku na poziomie zadania, aby sprawdzić, czy `github.ref` jest równy gałęzi scalania pull requesta.
```yaml
on:
    pull_request:
        types: [closed]
jobs:
    post-merge: 
        if: ${{ github.ref == github.event.pull_request.base.ref }}
``` 
> Po scaleniu pull requesta `github.ref` będzie *pełnym odniesieniem do gałęzi* scalania (np. `refs/heads/main`), a nie tylko nazwą gałęzi scalania (np. `main`).
