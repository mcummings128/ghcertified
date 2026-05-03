---
question: "マトリックス下記を使用するワークフローがあります。マトリックス内のジョブが失敗した場合に、進行中およびキューに入っている他のジョブがキャンセルされないようにするにはどうすればよいですか？"
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

- [x] `jobs.<job_id>.strategy.fail-fast` を `false` に設定する
> デフォルトでは `jobs.<job_id>.strategy.fail-fast` は `true` に設定されており、あるマトリックスジョブが失敗した場合、進行中およびキューに入っている他のマトリックスジョブはキャンセルされます。この動作を避けるためには、明示的に `fail-fast` を `false` に設定する必要があります。
- [ ] 何もする必要はない。`jobs.<job_id>.strategy.fail-fast` のデフォルト設定は `false` である
> デフォルトでは `jobs.<job_id>.strategy.fail-fast` は `true` に設定されています。
- [ ] `jobs.<job_id>.strategy.matrix.fail-fast` を `false` に設定する
> これは誤りです。`fail-fast` は `strategy` レベルで設定されるものであり、`matrix` レベルではありません。`fail-fast` を `matrix` レベルで設定しても、[ジョブの設定](https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/run-job-variations#adding-a-matrix-strategy-to-your-workflow-job)の一部として機能し、他のマトリックスジョブのキャンセルや継続には影響を与えません。
- [ ] 何もする必要はない。`jobs.<job_id>.strategy.matrix.fail-fast` のデフォルト設定は `false` である
> これは誤りです。`fail-fast` は `strategy` レベルで設定されるものであり、`matrix` レベルではありません。
- [ ] この動作を強制する方法はなく、回避することはできません。
