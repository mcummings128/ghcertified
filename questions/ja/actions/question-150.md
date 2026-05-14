---
question: "Dorothea はプッシュイベントによってトリガーされたワークフローをトラブルシューティングしており、Webhook の詳細を確認したいと考えています。トリガーとなった Webhook のペイロード全体をどのように確認できますか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] ステップ内で `github.event` オブジェクトの内容を出力する
> `github.event` は完全なイベント Webhook ペイロードを表示します。このペイロードはイベントの種類によって異なります。詳細は [Webhook events and payloads](https://docs.github.com/en/webhooks/webhook-events-and-payloads) を参照してください。
- [ ] ワークフロー実行オプションの「イベント Webhook ペイロードを表示」チェックボックスをオンにする。
- [ ] `SHOW_EVENT_PAYLOAD` という名前のシークレットまたは変数を `true` に設定する。
- [ ] リポジトリ設定の「Webhooks」セクションに移動する。
> リポジトリ設定の「Webhooks」セクションは、`push` のような標準的なイベント Webhook ではなく、カスタム Webhook の詳細のみを表示します。
