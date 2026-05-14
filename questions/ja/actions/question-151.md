---
question: "ジョブ間で情報を渡す際には、ジョブの出力または`GITHUB_ENV`のどちらを使用すべきですか？"
documentation: "https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/use-variables#passing-values-between-steps-and-jobs-in-a-workflow"
---

- [x] ジョブの出力、なぜなら、`GITHUB_ENV`に書き込むことで設定された環境変数の値は現在のジョブにのみ適用されるからです。
> `env`はワークフローレベルで設定可能で、複数のジョブ間で変数が参照可能であることを意味しますが、環境変数の値を変更してもそれが値を変更したジョブを超えて持続することはありません。
- [ ] `GITHUB_ENV`、なぜならジョブの出力は同じジョブ内でのみ設定および参照できるからです。
- [ ] ジョブの出力、なぜなら設定がより簡単だからです。
> ジョブの出力を設定して参照するのは、`GITHUB_ENV`を利用するよりも複雑です。たとえば、ジョブの出力には`outputs`ブロックの設定、ステップに`id`を追加し、依存関係を示すために`needs`を使用する必要があります。
- [ ] `GITHUB_ENV`、なぜなら環境変数を設定することでランナーへの負担が大幅に軽減され、ワークフローの実行時間が短縮されるからです。
