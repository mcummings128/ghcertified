---
question: "W jaki sposób `repository_dispatch` umożliwia systemom spoza GitHub wyzwalanie przepływu pracy?"
documentation: "https://docs.github.com/en/rest/repos/repos?apiVersion=2026-03-10#create-a-repository-dispatch-event"
---

- [x] Zewnętrzny system wysyła żądanie POST do GitHub API, aby utworzyć zdarzenie repository dispatch.
- [x] Przepływ pracy jest wyzwalany przez utworzenie zdarzenia repository dispatch 
> Wynikiem "Create a repository dispatch event" jest nowe zdarzenie `repository_dispatch` (webhook), które jest nasłuchiwane przez `on.repository_dispatch`. 
- [x] Klucz workflow `on.repository_dispatch.types` odpowiada parametrowi `event_type` w treści żądania, ograniczając przepływ pracy do wyzwalania tylko w odpowiedzi na istotne zdarzenia zewnętrzne 
> `on.repository_dispatch.types` pozwala definiować niestandardowe typy aktywności. Zobacz [dokumentację](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#repository_dispatch) dla przykładów ilustrujących, jak `on.repository_dispatch.types` i `event_type` są ze sobą powiązane.
- [ ] Zewnętrzny system wysyła żądanie PUT do GitHub API, aby utworzyć zdarzenie repository dispatch
> Poprawną metodą HTTP dla "Create a repository dispatch event" jest POST.
- [ ] Przepływ pracy jest wyzwalany przez żądanie POST wysłane do przepływu pracy za pomocą następującego punktu końcowego `/repos/OWNER/REPO/actions/workflows/<WORKFLOW_ID>/dispatches` 
> Ten punkt końcowy odpowiada utworzeniu zdarzenia workflow dispatch, a nie repository dispatch event. Ponadto, żądania związane z Actions powinny być kierowane do GitHub API – żądań API nie można wysyłać bezpośrednio do przepływu pracy.
- [ ] Klucz workflow `on.repository_dispatch.event_types` odpowiada parametrowi `event_type` w treści żądania, ograniczając przepływ pracy do wyzwalania tylko w odpowiedzi na istotne zdarzenia zewnętrzne
> Nie istnieje klucz `on.repository_dispatch.event_types`. Używany jest `on.repository_dispatch.types`, zgodnie z tym, jak inne zdarzenia wykorzystują `on.<event_name>.types` do filtrowania na podstawie aktywności.
