---
question: "Dorothea rozwiązuje problem w workflow, który jest uruchamiany przez zdarzenie push i chce zobaczyć szczegóły webhooka. Jak może wyświetlić cały payload webhooka, który uruchomił workflow?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] Wydrukowanie zawartości obiektu `github.event` w kroku
> `github.event` pokaże pełny payload webhooka zdarzenia. Ten payload różni się w zależności od typu zdarzenia. Zobacz [Webhook events and payloads](https://docs.github.com/en/webhooks/webhook-events-and-payloads) po więcej szczegółów.
- [ ] Zaznaczenie pola wyboru "Show event webhook payload" w opcjach uruchamiania workflow.
- [ ] Ustawienie sekretu lub zmiennej o nazwie `SHOW_EVENT_PAYLOAD` na `true`
- [ ] Przejście do sekcji "Webhooks" w ustawieniach repozytorium
> Sekcja "Webhooks" w ustawieniach repozytorium pokazuje tylko szczegóły dla niestandardowych webhooków, a nie standardowych webhooków zdarzeń, takich jak `push`.
