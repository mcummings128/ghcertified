---
question: "Quantos jobs serão executados na seguinte matriz?"
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
> Esta matriz produz 5 jobs com as seguintes combinações de matriz:

> `os:ubuntu-latest,version:1,comment-color:blue,error-color:red` 

> `os:ubuntu-latest,version:2,comment-color:blue,error-color:red` 

> `os:windows-latest,version:1,comment-color:green,error-color:red` 

> `os:windows-latest,version:2,comment-color:green,error-color:red` 

> `os:macos-latest,comment-color:yellow` 

> Uma chave `include` NÃO definida em `strategy.matrix` pode ser adicionada a uma configuração de job desde que não sobrescreva a configuração. Chaves `include` já presentes em `strategy.matrix` irão criar um novo job, se tiverem um novo valor. 

- [ ] 6
- [ ] 7
- [ ] 10
