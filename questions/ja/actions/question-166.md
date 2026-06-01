---
question: "JavaScriptアクションと`actions/github-script`はどちらもJavaScriptを使用します。独自のJavaScriptアクションを作成するのではなく、`actions/github-script`を使用するべき理由は何ですか？"
documentation: "https://github.com/actions/github-script"
---

- [x] `actions/github-script`は短いインラインスクリプトで使用するべきです
- [x] `actions/github-script`はGitHub APIとやり取りするための事前認証済みクライアントを使用したい場合に使用するべきです
- [x] JavaScriptアクションは複数のリポジトリ間で再利用可能なカスタムアクションを作成したい場合に使用するべきです
- [ ] JavaScriptアクションは短いインラインスクリプトで使用するべきです
- [ ] `actions/github-script`は、複数の特定の依存関係を持つ細かく調整されたNode.js環境を利用する必要がある場合に使用するべきです
> `actions/github-script`が使用される前にモジュールをインストールすることは可能ですが、依存関係が多いとワークフロー内で複数のステップが必要になります。また、`actions/github-script`ではNode.jsバージョンを変更することはできず、定義されたバージョンに限定されます。
- [ ] JavaScriptアクションはGitHub APIコールを行うためのオーバーヘッドが少ない解決策を探している場合に使用するべきです
> JavaScriptアクションはオーバーヘッドが少ないわけではありません。`action.yml`ファイルを作成する必要があり、それはアプローチによっては専用のフォルダや場合によっては専用のリポジトリに保存する必要があります。`actions/github-script`は事前認証済みのクライアントを備えており、JavaScriptを使用してGitHub APIコールを簡単に行うことができます。
