---
question: "Które z poniższych stwierdzeń są prawdziwe w porównaniu zdarzeń pull_request i pull_request_target?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request"
---

- [x] Zdarzenie `pull_request` działa w kontekście commita scalającego (merge commit), podczas gdy `pull_request_target` działa w kontekście domyślnej gałęzi bazowego repozytorium.
> Więcej informacji o commitach scalających można znaleźć w dokumentacji GitHub [documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges). 
- [x] Workflow nie uruchomią się przy aktywności `pull_request`, jeśli występuje konflikt scalania.
- [x] Zdarzenia `pull_request` i `pull_request_target` mają domyślny typ aktywności: `opened`, `synchronize` i `reopened`.
- [ ] `pull_request` powinno być używane ostrożnie, ponieważ PR-y z forków umożliwią workflow dostęp do wszystkich sekretów w repozytorium z powodu powiązania z domyślną gałęzią.
> To dotyczy `pull_request_target`; `pull_request` nie jest powiązane z domyślną gałęzią i dlatego, gdy jest uruchamiane przez PR-y z forków, workflow będzie mieć ograniczony dostęp do sekretów. Zobacz powyżej podlinkowaną dokumentację, w szczególności sekcję "pull_request_target", aby uzyskać więcej informacji.
- [ ] Workflow nie uruchomią się przy aktywności `pull_request_target`, jeśli występuje konflikt scalania.
- [ ] Zdarzenie `pull_request_target` powinno być używane, gdy chcesz uruchomić kod zawarty w zmienionych plikach PR-u, na przykład w celu wykonania testów CI lub uruchomienia zestawów testowych.
> `pull_request_target` działa w kontekście domyślnej gałęzi repozytorium, co może prowadzić do wykonania niezaufanego kodu w ramach aktywności, takiej jak testy CI lub zestawy testów. Zobacz [dokumentację](https://docs.github.com/en/enterprise-cloud@latest/actions/reference/security/secure-use#mitigating-the-risks-of-untrusted-code-checkout), aby uzyskać więcej informacji.
