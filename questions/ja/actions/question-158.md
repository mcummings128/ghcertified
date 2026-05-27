---
question: "Petra は、`post-merge` という名前のジョブだけを持つワークフローを作成しています。マージされた Pull Request をトリガーとしてジョブを設定するには、どうすればよいですか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#running-your-pull_request-workflow-when-a-pull-request-merges"
---

- [x]  `pull_request` アクティビティの種類を `closed` と指定し、ジョブレベルの条件文を使用して `github.event.pull_request.merged` が true であるかを確認する
```yaml
on:
    pull_request:
        types: [closed]

jobs:
    post-merge:
        if: github.event.pull_request.merged == true
``` 
> Pull Request がマージされたときにワークフロージョブをトリガーするには、`on:` で Pull Request のアクティビティの種類を指定し、ジョブレベルの条件を設定する必要があります。
- [ ]  `pull_request` アクティビティの種類を `merged` と指定し、ジョブレベルの条件文を使用して `github.event.pull_request.merged` が true であるかを確認する
```yaml
on:
    pull_request:
        types: [merged]
jobs:
    post-merge:
        if: github.event.pull_request.merged == true
``` 
> `pull_request` イベントには `merged` アクティビティの種類はありません。`pull_request` の有効なアクティビティの種類については、リンクされたドキュメントの "pull_request" セクションを参照してください。
- [ ]  `pull_request` アクティビティの種類を `merged` と指定する（ジョブレベルの条件文は不要）
```yaml
on:
    pull_request:
        types: [merged]
jobs:
    post-merge:
``` 
> `pull_request` イベントには `merged` アクティビティの種類はありません。
- [ ] `pull_request` アクティビティの種類を `closed` と指定する（ジョブレベルの条件文は不要）
```yaml
on:
    pull_request:
        types: [closed]
jobs:
    post-merge:
``` 
> Pull Request はマージされずに閉じられることもあります。Pull Request がマージされた場合にのみジョブを実行したい場合は、対応するジョブレベルの条件文を使用せずにこれを指定すると、Pull Request が閉じられるたびにジョブが発火してしまいます。
- [ ]  `pull_request` アクティビティの種類を `closed` と指定し、ジョブレベルの条件文を使用して `github.ref` が Pull Request のマージ先ブランチと等しいかを確認する
```yaml
on:
    pull_request:
        types: [closed]
jobs:
    post-merge: 
        if: ${{ github.ref == github.event.pull_request.base.ref }}
``` 
> Pull Request がマージされた後、`github.ref` はマージ先ブランチの完全な参照 (`refs/heads/main` など) となり、単純なブランチ名 (`main` など) ではありません。
