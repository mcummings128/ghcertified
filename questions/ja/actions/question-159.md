---
question: "次のうち、pull_requestイベントとpull_request_targetイベントを比較する際に正しいものはどれですか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request"
---

- [x] `pull_request`イベントはマージコミットのコンテキスト内で実行され、`pull_request_target`イベントはベースのリポジトリのデフォルトブランチのコンテキスト内で実行されます。
> マージコミットの詳細については、GitHubの[ドキュメント](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges)を参照してください。
- [x] マージコンフリクトがある場合、`pull_request`アクティビティでワークフローは実行されません。
- [x] `pull_request`および`pull_request_target`イベントのデフォルトのアクティビティタイプは`opened`、`synchronize`、および`reopened`です。
- [ ] `pull_request`はフォークからのPRがリポジトリ内のすべてのシークレットにアクセスできるため、注意して使用する必要があります。
> これは`pull_request_target`に当てはまります。`pull_request`はデフォルトブランチに関連付けられていないため、フォークされたPRによってトリガーされた場合、ワークフローはシークレットへのアクセスが制限されます。詳細については、上記のドキュメント内の「pull_request_target」のセクションを参照してください。
- [ ] マージコンフリクトがある場合、`pull_request_target`アクティビティでワークフローは実行されません。
- [ ] `pull_request_target`イベントは、CIチェックやテストスイートの実行など、PRの変更ファイルに含まれるコードを実行する場合に使用する必要があります。
> `pull_request_target`はリポジトリのデフォルトブランチのコンテキスト内で実行されるため、CIチェックやテストスイートなどのアクティビティにより信頼されていないコードがチェックアウトおよび実行される可能性があります。詳細については、[ドキュメント](https://docs.github.com/en/enterprise-cloud@latest/actions/reference/security/secure-use#mitigating-the-risks-of-untrusted-code-checkout)を参照してください。
