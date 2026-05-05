---
question: "Chcesz utworzyć workflow `Post-Deploy`, który wykonuje czynności związane z wdrożeniem. Jakiego wyzwalacza zdarzeń powinien użyć workflow `Post-Deploy`, aby uruchamiał się automatycznie po zakończeniu określonego workflow?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_run"
---

- [x] `workflow_run`
> `workflow_run` pozwala na uruchomienie workflow po zakończeniu innych określonych workflow (niezależnie od sukcesu). Należy zauważyć, że chociaż to pytanie dotyczy zakończonych workflow, `workflow_run` może być również skonfigurowany tak, aby wyzwalać workflow po uruchomieniu innych określonych workflow lub rozpoczęciu ich przetwarzania na runnerze.
- [ ] `workflow_trigger`
> Nie istnieje taki wyzwalacz zdarzeń.
- [ ] `workflow_dispatch`
> `workflow_dispatch` jest używane do ręcznego uruchamiania workflow. Zobacz [dokumentację](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_dispatch), aby uzyskać więcej informacji.
- [ ] `workflow_call`
> `workflow_call` jest używane do wywoływania workflow z innych workflow lub akcji. Zobacz [dokumentację](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_call), aby uzyskać więcej informacji.
