---
question: "Dlaczego warto ponownie uruchomić workflow zamiast generować nowe jego uruchomienie?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-workflow-runs/re-run-workflows-and-jobs"
---

- [x] Ponowne uruchomienie workflow pozwala na ponowne uruchomienie niepowodzących się zadań workflow, w przeciwieństwie do generowania nowego uruchomienia, które uruchamia wszystkie zadania.
- [x] Ponowne uruchomienie workflow oznacza, że zadania workflow są uruchamiane w tym samym kontekście commit SHA i odniesienia git (git ref) co oryginalne zdarzenie, które wywołało zadanie.
- [x] Ponowne uruchomienie workflow pozwala włączyć dodatkowe logowanie debugowania dla wybranych zadań.
- [ ] Ponowne uruchomienie workflow zapewnia, że `GITHUB_TRIGGERING_ACTOR` pozostaje niezmieniony, co eliminuje niejednoznaczność co do tego, kto pierwotnie uruchomił workflow.
> Zgodnie z [dokumentacją](https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context), wartość `GITHUB_TRIGGERING_ACTOR` jest aktualizowana na podstawie tego, kto ponownie uruchomił workflow.  
- [ ] Ponowne uruchomienie workflow zapewnia, że `GITHUB_ACTOR` jest aktualizowany, co pozwala jednoznacznie ustalić, kto ponownie uruchomił workflow.
> Zgodnie z [dokumentacją](https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context), wartość `GITHUB_ACTOR` dotyczy osoby, która pierwotnie uruchomiła workflow; nie zmienia się po ponownym uruchomieniu workflow.
- [ ] Ponowne uruchomienie workflow nadpisuje niepowodzące się uruchomienia zadań, sprawiając, że uruchomienia wydają się bardziej przejrzyste.
> Niepowodzące się uruchomienia zadań pozostają widoczne po ich ponownym uruchomieniu. Korzystając z interfejsu użytkownika, łatwo jest przełączać się między oryginalnym uruchomieniem zadania a kolejnymi ponownymi uruchomieniami.  
