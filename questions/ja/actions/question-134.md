---
question: "GitHub Actions ワークフローでカスタム JavaScript スクリプトを直接実行するにはどうすればよいですか？"
documentation: "https://github.com/marketplace/actions/github-script"
---

- [x] `actions/github-script` アクションを使用する
> `actions/github-script` を使用すると、API コールを行い、ワークフローのコンテキストにアクセスするためのインライン JavaScript を記述して活用できます。`actions/github-script` を使用するには、[ドキュメント](https://github.com/actions/github-script) に記載されているように、他のアクションと同様に呼び出すだけです。
- [ ] リポジトリの Actions 設定で「Allow custom JavaScript scripts」構成を有効にする
> リポジトリの Actions 設定に「Allow custom JavaScript scripts」構成はありません。
- [ ] 組織の Actions 設定で「Allow custom JavaScript scripts」構成を有効にする
> リポジトリの Actions 設定に「Allow custom JavaScript scripts」構成はありません。公式 GitHub Actions を使用するには、組織の Actions 設定で「Allow actions created by GitHub」のような設定を有効にする必要がある場合がありますが、これは `actions/github-script` のみに関連するものではありません。
- [ ] スクリプトブロックの内容を `GITHUB_SCRIPT` 環境変数に書き込む
> `GITHUB_SCRIPT` はデフォルトの GitHub Actions 環境変数ではありません。デフォルトの環境変数のリストは、[ドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/variables) に記載されています。
- [ ] JavaScript アクションで `using` キーを `'github-script'` に設定する
> JavaScript アクションでは、`using` キーをサポートされている Node.js のバージョンを指定するために `node*` に設定する必要があります。通常、JavaScript アクションは `actions/github-script` を必要としません。
