---
question: "ワークフローが`pull_request`イベントによってトリガーされた場合、`github.ref`に関して正しい記述はどれですか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] マージされていないプルリクエストでは、`github.ref`はプルリクエストのマージブランチ/タグの完全なrefを指します。
> 例えば、(オープンされている) プルリクエストの番号が#123の場合、`github.ref`は`refs/pull/123/merge`となります。refに関する詳細は、公式の[Gitドキュメント](https://git-scm.com/book/en/Git-Internals-Git-References)をご参照ください。
- [x] マージ済みのプルリクエストでは、`github.ref`はマージ先のブランチの完全なrefを指します。
> 例えば、`main`ブランチに何かをマージした場合、プルリクエストがマージされた後の`github.ref`は`ref/heads/main`となります。
- [ ] プルリクエスト (マージ状態にかかわらず)では、`github.ref`はプルリクエスト番号を指します。
> `pull_request`イベントでは、`github.ref`の値はプルリクエストがマージされたかどうかによって異なります。この値は常にrefであり、プルリクエスト番号ではありません。
- [ ] プルリクエスト (マージ状態にかかわらず)では、`github.ref`は`GITHUB_REF`ブランチ上の最後のマージコミットのSHAです。
> `github.sha`はマージブランチ上の最新のSHAを指します (例: `refs/pull/PULL_REQUEST_NUMBER/merge`)。詳細については、[イベントのドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request) (`GITHUB_SHA`を検索)をご参照ください。
- [ ] マージされていないプルリクエストでは、`github.ref`はプルリクエストのタイトルの完全なrefです。
> refはプルリクエストタイトルから形成されません。`github.event.pull_request.title`がプルリクエストタイトルを含みます。詳しくは、[ドキュメント](https://docs.github.com/en/webhooks/webhook-events-and-payloads#pull_request)をご参照ください。
- [ ] マージ済みのプルリクエストでは、`github.ref`はワークフローの実行をトリガーした完全なrefの種類です。この値は`branch`、`tag`、または(完全に形成されていない場合)`null`になります。
> `github.ref_type`はワークフローの実行をトリガーしたrefの種類を示す値です。この値には`branch`または`tag`のみが含まれます。`null`は有効な値ではありません。詳細については、この質問内のドキュメントリンクを参照してください。
