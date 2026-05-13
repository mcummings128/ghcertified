---
question: "`pull_request` イベントによってワークフローがトリガーされた場合、`github.ref` に関するどの記述が正しいですか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] マージされていない Pull Request では、`github.ref` は Pull Request マージブランチ/タグの完全な ref を指します。  
> ref に関する詳細は、公式の [Git ドキュメント](https://git-scm.com/book/en/Git-Internals-Git-References) を参照してください。
- [x] マージ済みの Pull Request では、`github.ref` はマージ先ブランチの完全な ref を指します。  
- [ ] Pull Request (マージ状態にかかわらず) では、`github.ref` が Pull Request 番号を指します。  
> `pull_request` イベントでは、Pull Request のマージ状態によって `github.ref` の値が異なります。この値は常に ref であり、Pull Request 番号ではありません。
- [ ] Pull Request (マージ状態にかかわらず) では、`github.ref` が `GITHUB_REF` ブランチの最後のマージコミットの SHA です。  
> `github.sha` がマージブランチ上の最新 SHA を指します (例: `refs/pull/PULL_REQUEST_NUMBER/merge`)。詳細については [イベントのドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request) を参照してください (`GITHUB_SHA` を検索)。
- [ ] マージされていない Pull Request では、`github.ref` が Pull Request タイトルの完全な ref です。  
> ref は Pull Request タイトルから形成されません。`github.event.pull_request.title` が Pull Request タイトルを保持するものです。詳しくは [ドキュメント](https://docs.github.com/en/webhooks/webhook-events-and-payloads#pull_request) を参照してください。
- [ ] マージ済みの Pull Request では、`github.ref` がワークフロー実行をトリガーした ref のタイプ (完全な形で) となり、その値は `branch`、`tag`、または (ref が完全に形成されなかった場合は) `null` です。  
> `github.ref_type` がワークフロー実行をトリガーした ref のタイプの値です。この値には `branch` または `tag` のみが含まれ、`null` は有効な値ではありません。この質問内のドキュメントリンクを参照してください。
