---
question: "Hilda potrzebuje dostępu do artefaktu wygenerowanego przez ostatnie uruchomienie workflow, ale sam plik workflow został od tego czasu usunięty. Czy nadal będzie mogła odzyskać artefakt?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-workflow-runs/remove-workflow-artifacts#artifacts-from-deleted-workflow-runs"
---

- [x] Tak, ponieważ usunięcie workflow nie powoduje automatycznego usunięcia jego uruchomień i wygenerowanych artefaktów
> Uruchomienia workflow i ich wygenerowane artefakty nie są automatycznie usuwane, gdy odpowiadający im workflow zostanie usunięty. Aby usunąć artefakty, należy usunąć samo uruchomienie.
- [ ] Nie, ponieważ usunięcie workflow automatycznie usuwa jego uruchomienia i wygenerowane artefakty
- [ ] Tak, ale tylko jeśli ma uprawnienia administratora
- [ ] Nie, ponieważ chociaż uruchomienia workflow pozostaną po usunięciu workflow, wygenerowane artefakty ulegają uszkodzeniu
