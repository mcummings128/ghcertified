---
question: "Ile zadań zostanie uruchomionych w poniższej macierzy?"
documentation: "https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/run-job-variations#expanding-or-adding-matrix-configurations"
---

```yaml
jobs:
  test_deploy:
    strategy:
      matrix:
        os: [ubuntu-latest, windows-latest]
        version: [1, 2]
        include:
            - comment-color: "green"
            - error-color: "red"
            - os: "ubuntu-latest"
              comment-color: "blue"
            - os: "macos-latest"
              comment-color: "yellow"
```

- [x] 5
> Ta macierz generuje 5 zadań z następującymi kombinacjami macierzy:

> `os:ubuntu-latest,version:1,comment-color:blue,error-color:red` 

> `os:ubuntu-latest,version:2,comment-color:blue,error-color:red` 

> `os:windows-latest,version:1,comment-color:green,error-color:red` 

> `os:windows-latest,version:2,comment-color:green,error-color:red` 

> `os:macos-latest,comment-color:yellow` 

> Klucz `include` NIE zdefiniowany w `strategy.matrix` może zostać dodany do konfiguracji zadania, jeśli nie nadpisuje konfiguracji. Klucze `include` już obecne w `strategy.matrix` utworzą nowe zadanie, jeśli mają nową wartość.

- [ ] 6
- [ ] 7
- [ ] 10
