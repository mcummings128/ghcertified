---
question: "アネットは、彼女のプライベートなOrganization内のメンバーだけが使用するカスタム`npm`パッケージを公開するためのWorkflowを作成する必要があります。彼女のWorkflowには何を含めるべきですか？"
documentation: "https://docs.github.com/en/packages/learn-github-packages/publishing-a-package"
---

- [x] GitHub Packagesに公開するためのロジック
> GitHub PackagesはGitHubに統合されたパッケージレジストリで、GitHub固有のニーズ（ActionsやWorkflowsなど）に対応する場合には特に使いやすいです。GitHub Packagesにはパッケージをプライベートにホストする機能が含まれています。
- [x] `write:packages`権限を持つトークン
> 個人アクセストークンはすべてのGitHub Packagesレジストリでサポートされています。特定のレジストリでは`GITHUB_TOKEN`の使用もサポートされています。詳細については[ドキュメント](https://docs.github.com/en/packages/learn-github-packages/about-permissions-for-github-packages#about-scopes-and-permissions-for-package-registries)を参照してください。
- [x] 対応するGitHub Packagesレジストリ`https://npm.pkg.github.com`との通信ロジック
> GitHub Packagesに関連するWorkflowは、対応するGitHubホストのパッケージレジストリとの通信を伴うことがよくあります。このレジストリのURLの構文は`https://<package-type>.pkg.github.com`です。例については、[npmレジストリのドキュメント](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry)を参照してください。
- [ ] `on:registry_package`イベント（アクティビティタイプを指定しないもの）
> `on:registry_package`はパッケージに関連するものですが、パッケージを公開するためにこのイベントはWorkflowに必要ありません。
- [ ] `admin:packages`権限を持つトークン
> `admin:packages`権限はGitHub Packagesにホストされているパッケージを削除する場合にのみ必要です。このケースでは、必要最小限の権限の原則に従い、`write`権限のみが必要です。
- [ ] `types:[published]`を指定した`on:registry_package`イベント
> `on:registry_package`イベントは、パッケージが公開されたときにWorkflowをトリガーするよう構成できますが、パッケージを公開するためにこのイベントはWorkflowに必要ありません。
