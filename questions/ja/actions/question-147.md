---
question: "GitHub Actionsのワークフロー内でBase64でエンコードされたシークレットをデコードします。デコードしたシークレットが誤ってワークフローログに表示されないようにするにはどうすればよいですか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-commands#masking-a-value-in-a-log"
---

- [x] デコードされたシークレットが使用されるジョブで、`add-mask` ワークフローコマンドを使用する。
> `add-mask` を使用すると、GitHub Actionsがシークレットとして検出しない値を編集できます。これは、デコードされたシークレットを使用するジョブごとに、値ごとに1回行う必要があります。
- [ ] 何もする必要はありません。GitHub Actionsインフラストラクチャが自動的にデコードされたシークレットを編集します。
> [ドキュメント](https://docs.github.com/en/actions/reference/security/secure-use#use-secrets-for-sensitive-information) によれば、GitHub Actionsが変換されたシークレットを自動的に検出して編集することを保証するものではありません。
- [ ] デコードされたシークレットを含むprint文を回避する。この方法が唯一、デコードされたシークレットがワークフローログに表示されるのを防ぐ手段であるため。
> デコードされたシークレットを含むprint文を回避することは推奨されますが、デコードされたシークレットはAPI呼び出しに関するメッセージなど、ワークフローログの他の場所にも表示される可能性があります。
- [ ] デコードされたシークレットが使用される場合、組み込みの `maskSecret` 関数を使用してそれを編集する。
> `maskSecret` はGitHub Actionsによって提供される組み込み関数ではありません。
