---
question: "以下のマトリックスで実行されるジョブは何個ですか？"
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
> このマトリックスは以下の組み合わせで5つのジョブを生成します:

> `os:ubuntu-latest,version:1,comment-color:blue,error-color:red` 

> `os:ubuntu-latest,version:2,comment-color:blue,error-color:red` 

> `os:windows-latest,version:1,comment-color:green,error-color:red` 

> `os:windows-latest,version:2,comment-color:green,error-color:red` 

> `os:macos-latest,comment-color:yellow` 

> `strategy.matrix` で定義されていない `include` キーは、設定を上書きしない場合にジョブ設定に追加することができます。`strategy.matrix` ですでに存在する `include` キーは、新しい値がある場合に新しいジョブを作成します。

- [ ] 6
- [ ] 7
- [ ] 10
