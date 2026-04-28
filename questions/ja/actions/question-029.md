---
question: "プルリクエスト分析ワークフローでは複数のコード分析ツールを使用し、完了するまでに約20分かかります。このワークフローは`pull_request`イベントでトリガーされ、`branches`フィルターが`master`に設定されています。そのため、開発者が数分以内に複数のコミットをプッシュすると、複数のワークフローが並行して実行されます。すべての以前のワークフロー実行を停止し、最新の変更のみを実行するにはどうすればよいですか？"
documentation: "https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#example-using-concurrency-to-cancel-any-in-progress-job-or-run"
---

- [x] 同時実行とキャンセルインプログレスを使用
```yaml
concurrency:
  group: ${{ github.workflow }}-${{ github.ref }}
  cancel-in-progress: true
```
- [ ] 同時実行を使用
```yaml
concurrency:
  group: ${{ github.ref }}
```
> これはそのgithub ref上の実行をキューに入れます。以前の実行を停止することはありません

- [ ] アクティビティタイプフィルターを使用
```yaml
on:
  pull_request:
    branches:
      - master
    types: [latest]
```
> `pull_request`イベントには`latest`というアクティビティタイプはありません

- [ ] `pull_request`イベントの`cancel-in-progress`フラグを使用
```yaml
on:
  pull_request:
    branches:
      - master
    cancel-in-progress: true
```
> `cancel-in-progress`は`concurrency`ブロックの中でのみ使用できます。これは`pull_request`の有効なキーではありません。
