---
question: "GitHub ActionsワークフローでカスタムJavaScriptスクリプトを直接実行するにはどうすればよいですか？"
documentation: "https://github.com/marketplace/actions/github-script"
---

- [x] `actions/github-script`アクションを使用
> `actions/github-script`を使用すると、インラインJavaScriptを記述してAPI呼び出しを行ったり、ワークフローコンテキストにアクセスしたりできます。`actions/github-script`を使用するには、[ドキュメント](https://github.com/actions/github-script)に記載されているように、他のアクションと同じように呼び出します。
- [ ] リポジトリのActions設定で「カスタムJavaScriptスクリプトを許可する」設定を有効化する
> リポジトリのActions設定には「カスタムJavaScriptスクリプトを許可する」という設定は存在しません。
- [ ] 組織のActions設定で「カスタムJavaScriptスクリプトを許可する」設定を有効化する
> リポジトリのActions設定には「カスタムJavaScriptスクリプトを許可する」という設定は存在しません。公式のGitHub Actionsを使用するには、組織のAction設定で「GitHubによって作成されたアクションを許可する」などの設定を有効にする必要がある場合がありますが、これは`actions/github-script`にのみ関連するものではありません。
- [ ] スクリプトブロックの内容を`GITHUB_SCRIPT`環境変数に書き込む
> `GITHUB_SCRIPT`はデフォルトのGitHub Actions環境変数ではありません。デフォルト環境変数のリストは[ドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/variables)で確認できます。
- [ ] JavaScriptアクションで`using`キーを`'github-script'`に設定する
> JavaScriptアクションでは、`using`キーを`node*`（*はサポートされているNode.jsのバージョン）に設定する必要があります。一般的に、JavaScriptアクションでは`actions/github-script`を使用する必要はありません。
