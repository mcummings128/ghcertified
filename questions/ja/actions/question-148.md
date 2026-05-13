---
question: "ワークフローが push イベントによってトリガーされる場合、`github.ref` に関する記述のうち正しいものはどれですか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] push イベントでは、`github.ref` はプッシュされたブランチまたはタグの完全な ref を指します。  
> ref に関する詳細は、公式の [Git ドキュメント](https://git-scm.com/book/en/Git-Internals-Git-References) を参照してください。
- [ ] push イベントでは、`github.ref` はワークフローをトリガーしたコミットのメッセージを指します。  
> 最新のコミットメッセージは `github.event.head_commit.message` に含まれます。詳細は [ドキュメント](https://docs.github.com/en/webhooks/webhook-events-and-payloads#push) を参照してください。
- [ ] push イベントでは、`github.ref` はワークフローをトリガーしたコミットの SHA を指します。  
> `github.sha` がコミット SHA を指します。この質問内のドキュメントリンクおよび [イベントドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows) を参照してください。
- [ ] push イベントでは、`github.ref` はワークフローをトリガーしたコミットの説明を指します。
- [ ] push イベントでは、`github.ref` はワークフローの実行をトリガーした完全な ref の種類を指します。この値は `branch`、`tag`、または（ref が完全でない場合）`null` のいずれかになります。  
> `github.ref_type` がワークフロー実行をトリガーした ref の種類を指す値です。この値には `branch` または `tag` のみが含まれ、`null` は有効な値ではありません。この質問内のドキュメントリンクを参照してください。
