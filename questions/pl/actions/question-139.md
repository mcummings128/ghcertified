---
question: "W jaki sposób można włączyć logowanie diagnostyczne biegacza?"
documentation: "https://docs.github.com/en/actions/how-tos/monitor-workflows/enable-debug-logging#enabling-runner-diagnostic-logging"
---

- [x] Ustawienie sekretu lub zmiennej o nazwie `ACTIONS_RUNNER_DEBUG` na `true`
> Uwaga: `ACTIONS_RUNNER_DEBUG` można ustawić jako sekret lub zmienną na poziomie organizacji lub repozytorium.
- [x] Ponowne uruchomienie przepływu pracy z włączonym `Enable debug logging`
- [ ] Poprzez dodanie folderu najwyższego poziomu `ACTIONS_RUNNER_DEBUG` do repozytorium przepływu pracy
- [ ] Poprzez dodanie podfolderu `runner-diagnostic-logs` do katalogu `_diag` używanego biegacza hostowanego samodzielnie
> `runner-diagnostic-logs` to nazwa folderu, który generuje GitHub, gdy `ACTIONS_RUNNER_DEBUG` jest włączona. Aby uniknąć potencjalnych nieporozumień, folder o tej nazwie nie powinien być tworzony w innym miejscu. 
- [ ] Zmiana nazwy katalogu `_diag` biegacza hostowanego samodzielnie na `runner-diagnostic-logs`
> Zmienianie nazwy katalogu `_diag` nigdy nie powinno być wykonywane, ponieważ może to potencjalnie wpłynąć na działania logowania.
