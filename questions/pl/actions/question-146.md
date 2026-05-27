---
question: "Które stwierdzenia dotyczące `github.ref` są prawdziwe, gdy workflow jest wywoływany przez zdarzenie `pull_request`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] W przypadkach, gdy pull request nie został scalony, `github.ref` odnosi się do pełnego odwołania gałęzi/tagu scalającego pull request 
> Na przykład, jeśli numer (otwartego) pull requesta wynosił #123, `github.ref` będzie równy `refs/pull/123/merge`. Aby uzyskać więcej informacji o odniesieniach (refs), zobacz oficjalną [dokumentację Git](https://git-scm.com/book/en/Git-Internals-Git-References).
- [x] W przypadkach, gdy pull request został scalony, `github.ref` odnosi się do pełnego odwołania gałęzi, do której został włączony.
> Na przykład, jeśli coś zostało scalone do gałęzi `main`, `github.ref` będzie równy `ref/heads/main` po scaleniu pull requesta.
- [ ] W pull requestach (niezależnie od statusu scalania), `github.ref` odnosi się do numeru pull requesta 
> W przypadku zdarzenia `pull_request`, wartość `github.ref` zależy od tego, czy pull request został scalony. Ta wartość zawsze będzie odniesieniem (ref), a nie numerem pull requesta.
- [ ] W pull requestach (niezależnie od statusu scalania), `github.ref` to SHA ostatniego commita scalającego na gałęzi `GITHUB_REF`.
> `github.sha` wskazuje ostatni SHA na gałęzi scalającej (np. `refs/pull/PULL_REQUEST_NUMBER/merge`). Odwołaj się do [dokumentacji zdarzeń](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request) po więcej szczegółów (wyszukaj `GITHUB_SHA`).
- [ ] W przypadku pull requestów, które nie zostały scalone, `github.ref` to pełne odwołanie tytułu pull requesta. 
> Odniesienia (refs) nie są tworzone na podstawie tytułów pull requestów. `github.event.pull_request.title` zawiera tytuł pull requesta. Zobacz [dokumentację](https://docs.github.com/en/webhooks/webhook-events-and-payloads#pull_request) po więcej szczegółów.
- [ ] W przypadkach, gdy pull request został scalony, `github.ref` wskazuje rodzaj pełnego odwołania, które uruchomiło uruchomienie workflow. Wartość ta będzie `branch`, `tag` lub `null` (jeśli odniesienie nie było pełne).
> `github.ref_type` to wartość rodzaju odwołania, które wywołało uruchomienie workflow. Może zawierać tylko `branch` lub `tag`; `null` nie jest prawidłową wartością. Aby uzyskać więcej informacji, zapoznaj się z linkiem do dokumentu z tego pytania.
