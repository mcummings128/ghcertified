---
question: "Masz przepływ pracy, który korzysta z poniższej macierzy. Jak upewnić się, że inne trwające i oczekujące zadania w macierzy nie zostaną anulowane, jeśli jedno zadanie w macierzy zakończy się niepowodzeniem?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#jobsjob_idstrategyfail-fast"
---

```yaml
jobs:
  deploy:
    strategy:
      matrix:
        version: ["1", "1.2", "1.3"]
        os: [ubuntu-latest, windows-latest]
```

- [x] Ustaw `jobs.<job_id>.strategy.fail-fast` na `false`
> Domyślnie `jobs.<job_id>.strategy.fail-fast` ma wartość `true`, co oznacza, że jeśli jedno zadanie w macierzy zakończy się niepowodzeniem, inne trwające i oczekujące zadania w macierzy zostaną anulowane. Aby uniknąć tego zachowania, musisz jawnie ustawić `fail-fast` na `false`.
- [ ] Nic nie trzeba robić, ponieważ domyślne ustawienie `jobs.<job_id>.strategy.fail-fast` wynosi `false`
> Domyślnie `jobs.<job_id>.strategy.fail-fast` ma wartość `true`.
- [ ] Ustaw `jobs.<job_id>.strategy.matrix.fail-fast` na `false`
> To jest niepoprawne, `fail-fast` znajduje się na poziomie `strategy`, a nie `matrix`. Jeśli ustawisz `fail-fast` na poziomie `matrix`, będzie to element [konfiguracji zadania](https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/run-job-variations#adding-a-matrix-strategy-to-your-workflow-job) i nie wpłynie na anulowanie/kontynuację innych zadań w macierzy.
- [ ] Nic nie trzeba robić, ponieważ domyślne ustawienie `jobs.<job_id>.strategy.matrix.fail-fast` wynosi `false`
> To jest niepoprawne, `fail-fast` znajduje się na poziomie `strategy`, a nie `matrix`.
- [ ] Nie ma możliwości wymuszenia tego zachowania, nie ma obejścia tego problemu.
