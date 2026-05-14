---
question: "Czego należy używać do przekazywania informacji między zadaniami: wyników zadań czy `GITHUB_ENV`?"
documentation: "https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/use-variables#passing-values-between-steps-and-jobs-in-a-workflow"
---

- [x] Wyników zadań, ponieważ wartość zmiennych środowiskowych ustawionych za pomocą zapisu do `GITHUB_ENV` dotyczy tylko bieżącego zadania.
> Choć `env` można ustawić na poziomie przepływu pracy (co oznacza, że jego zmienne mogą być odwoływane przez wiele zadań), nie oznacza to, że zmiana wartości zmiennej środowiskowej jest utrzymywana poza zadaniem, które ją zmieniło.
- [ ] `GITHUB_ENV`, ponieważ wyniki zadań można ustawiać i odwoływać tylko w ramach jednego zadania.
- [ ] Wyników zadań, ponieważ są prostsze do skonfigurowania.
> Konfigurowanie i odwoływanie się do wyników zadań jest bardziej skomplikowane niż korzystanie z `GITHUB_ENV`. Na przykład wyniki zadań wymagają skonfigurowania bloku `outputs`, dodania `id` do kroku oraz użycia `needs`, aby wskazać zależności.
- [ ] `GITHUB_ENV`, ponieważ używanie go do ustawiania zmiennych środowiskowych znacznie zmniejsza obciążenie agenta, skracając czas wykonywania przepływu pracy.
