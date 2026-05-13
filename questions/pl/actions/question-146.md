---
question: "Które stwierdzenia dotyczące `github.ref` są prawdziwe, gdy workflow jest uruchamiany przez zdarzenie `pull_request`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] W przypadku pull requestów, które nie zostały scalone, `github.ref` odnosi się do w pełni ukształtowanego odniesienia gałęzi/tagu scalania pull requesta 
> Aby uzyskać więcej informacji o odniesieniach (refs), zobacz oficjalną [dokumentację Git](https://git-scm.com/book/en/Git-Internals-Git-References).
- [x] W przypadku pull requestów, które zostały scalone, `github.ref` odnosi się do w pełni ukształtowanego odniesienia gałęzi, do której wykonano scalenie.
- [ ] W przypadku pull requestów (niezależnie od statusu scalania), `github.ref` odnosi się do numeru pull requesta 
> Dla zdarzenia `pull_request` wartość `github.ref` różni się w zależności od tego, czy pull request został scalony. Ta wartość zawsze będzie odniesieniem (ref), a nie numerem pull requesta.
- [ ] W przypadku pull requestów (niezależnie od statusu scalania), `github.ref` jest wartością SHA ostatniego commita scalającego na gałęzi `GITHUB_REF`.
> `github.sha` wskazuje na najnowszy SHA na gałęzi scalającej (np. `refs/pull/PULL_REQUEST_NUMBER/merge`).  Zobacz [dokumentację dotyczącą zdarzeń](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request) po więcej szczegółów (poszukaj `GITHUB_SHA`).
- [ ] W przypadku pull requestów, które nie zostały scalone, `github.ref` jest w pełni ukształtowanym odniesieniem tytułu pull requesta. 
> Odniesienia (refs) nie są tworzone na podstawie tytułów pull requestów. `github.event.pull_request.title` zawiera tytuł pull requesta. Zobacz [dokumentację](https://docs.github.com/en/webhooks/webhook-events-and-payloads#pull_request) po więcej szczegółów.
- [ ] W przypadku pull requestów, które zostały scalone, `github.ref` jest rodzajem w pełni ukształtowanego odniesienia, które wywołało uruchomienie workflow. Wartość będzie `branch`, `tag` lub `null` (jeśli odniesienie nie było w pełni ukształtowane).
> `github.ref_type` to wartość typu odniesienia, które wywołało uruchomienie workflow. Może zawierać tylko wartości `branch` lub `tag`; `null` nie jest prawidłową wartością. Odwołaj się do linku dokumentacyjnego w tym pytaniu po więcej szczegółów.
