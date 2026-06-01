---
question: "どのようにして`repository_dispatch`はGitHub外部のシステムがワークフローをトリガーすることを可能にしますか？"
documentation: "https://docs.github.com/en/rest/repos/repos?apiVersion=2026-03-10#create-a-repository-dispatch-event"
---

- [x] 外部システムがGitHub APIにPOSTリクエストを送信して、リポジトリディスパッチイベントを作成する。
- [x] リポジトリディスパッチイベントの作成によってワークフローがトリガーされる。
> "Create a repository dispatch event"の結果は、新しい`repository_dispatch`イベント（Webhook）であり、これは`on.repository_dispatch`がリッスンしている。
- [x] `on.repository_dispatch.types`ワークフローキーはリクエストペイロード内の`event_type`パラメータに対応しており、ワークフローが関連する外部イベントでのみトリガーされるように制限されている。
> `on.repository_dispatch.types`を使用してカスタムアクティビティタイプを定義できます。`on.repository_dispatch.types`と`event_type`がどのように関連しているかについての例は[ドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#repository_dispatch)を参照してください。
- [ ] 外部システムがGitHub APIにPUTリクエストを送信して、リポジトリディスパッチイベントを作成する。
> "Create a repository dispatch event"に適切なHTTPメソッドはPOSTです。
- [ ] ワークフローは、エンドポイント`/repos/OWNER/REPO/actions/workflows/<WORKFLOW_ID>/dispatches`を使用して、ワークフローにPOSTリクエストを送信することでトリガーされる。
> このエンドポイントはリポジトリディスパッチイベントではなく、ワークフローディスパッチイベントを作成するためのものです。また、GitHub APIがActions関連のリクエスト送信に対応しているため、ワークフロー自体にAPIコールを行うことはできません。
- [ ] `on.repository_dispatch.event_types`ワークフローキーはリクエストペイロード内の`event_type`パラメータに対応しており、ワークフローが関連する外部イベントでのみトリガーされるように制限されている。
> `on.repository_dispatch.event_types`キーは存在しません。他のイベントがアクティビティに基づいてフィルタリングする際に`on.<event_name>.types`を使用するのと同様に、`on.repository_dispatch.types`が使用されます。
