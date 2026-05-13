---
question: "Które stwierdzenie jest prawdziwe w odniesieniu do `github.ref`, gdy workflow jest uruchamiany przez zdarzenie push?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] W zdarzeniach push, `github.ref` to pełny odnośnik gałęzi lub tagu, który został wypchnięty.
> Aby uzyskać więcej informacji na temat odnośników (refs), zobacz oficjalną [dokumentację Git](https://git-scm.com/book/en/Git-Internals-Git-References).
- [ ] W zdarzeniach push, `github.ref` to wiadomość commitu, który wywołał workflow.
> `github.event.head_commit.message` zawiera najnowszą wiadomość commitu. Zobacz [dokumentację](https://docs.github.com/en/webhooks/webhook-events-and-payloads#push) po więcej szczegółów.
- [ ] W zdarzeniach push, `github.ref` to SHA commitu, który wywołał workflow.
> `github.sha` wskazuje na SHA commitu. Odnieś się do [dokumentacji zdarzeń](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows) oraz linku w tym pytaniu, aby uzyskać więcej szczegółów.
- [ ] W zdarzeniach push, `github.ref` to opis commitu, który wywołał workflow.
- [ ] W zdarzeniach push, `github.ref` to typ w pełni utworzonego odnośnika, który wywołał uruchomienie workflow. Wartością będzie `branch`, `tag` lub `null` (jeśli odnośnik nie był w pełni utworzony).
> `github.ref_type` to wartość typu odnośnika, który wywołał uruchomienie workflow. Może zawierać tylko `branch` lub `tag`; `null` nie jest prawidłową wartością. Zobacz link do dokumentacji w tym pytaniu, aby uzyskać więcej szczegółów.
