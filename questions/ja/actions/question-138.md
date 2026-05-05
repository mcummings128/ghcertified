---
question: "デプロイ後の関連作業を実行するワークフロー `Post-Deploy` を作成したいと考えています。指定したワークフローが完了した後に自動的に実行されるようにするには、`Post-Deploy` ワークフローでどのイベントトリガーを使用する必要がありますか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_run"
---

- [x] `workflow_run`
> `workflow_run` を使用すると、指定した他のワークフローが完了した後に（成功の有無にかかわらず）ワークフローをトリガーできます。この質問では、完了したワークフローに特化していますが、`workflow_run` は他の指定されたワークフローがトリガーされたときや、ランナー上で処理を開始したときにワークフローをトリガーするようにも設定できます。
- [ ] `workflow_trigger`
> このようなイベントトリガーは存在しません。
- [ ] `workflow_dispatch`
> `workflow_dispatch` はワークフローを手動でトリガーするために使用されます。詳細は [ドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_dispatch) を参照してください。
- [ ] `workflow_call`
> `workflow_call` は、他のワークフローやアクションからワークフローを呼び出すために使用されます。詳細は [ドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_call) を参照してください。
