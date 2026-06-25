---
question: "Judith ma workflow, który powinien być uruchamiany za każdym razem, gdy w repozytorium zostanie wykonany commit. Repozytorium nie jest zawsze aktywne, więc Judith chce, aby workflow uruchamiał się programowo raz w tygodniu jako zabezpieczenie. Jakiej kombinacji zdarzeń powinna użyć, aby wymusić takie zachowanie?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows"
---

- [x] `push` i `schedule`
- [ ] `pull_request` (z `types:[closed]`) i `schedule`
> Pull requests mogą być zamykane bez ich scalania, a commity mogą być wykonywane w repozytorium bez pull requesta.
- [ ] `push` i `workflow_dispatch`
> W pytaniu użyto słowa „programowo”, co oznacza, że workflow powinien być uruchamiany w sposób automatyczny, a nie ręczny. Wymóg ręcznego uruchamiania workflow raz w tygodniu nie jest niezawodny — powinno to i może być zautomatyzowane za pomocą `schedule`.
- [ ] `push` i `weekly`
> `weekly` nie jest prawidłowym zdarzeniem. Użyj `schedule` z składnią `cron`, aby ustawić uruchamianie workflow raz w tygodniu.
- [ ] To nie jest możliwe: `schedule` nie może być łączone z innymi zdarzeniami
