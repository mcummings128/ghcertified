---
question: "Jakie jest zachowanie powiadomień, gdy GitHub przeprowadza skanowanie tajnych danych we wszystkich historycznych kodach w repozytoriach enterprise?"
documentation: "https://docs.github.com/en/code-security/secret-scanning/managing-alerts-from-secret-scanning/monitoring-alerts#historical-scans"
---

- [x] GitHub powiadamia właścicieli enterprise i menedżerów ds. bezpieczeństwa, nawet jeśli nie znaleziono żadnych tajnych danych.
- [x] GitHub powiadamia administratorów Repository, menedżerów ds. bezpieczeństwa oraz użytkowników z niestandardowymi rolami z dostępem do odczytu/zapisu za każdym razem, gdy wykryje tajne dane w repozytorium.
- [ ] GitHub powiadamia właścicieli enterprise i menedżerów ds. bezpieczeństwa tylko wtedy, gdy wykryje ujawnione tajne dane.
- [ ] GitHub powiadamia autorów commita zawierającego ujawnione tajne dane.
