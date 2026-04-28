---
question: "GitHub Enterprise Server を使用している組織が、GitHub.com 上でホストされているサードパーティ GitHub Actions を GitHub Enterprise Server インスタンスに自動同期するにはどうすればよいですか？"
documentation: "https://docs.github.com/ja/enterprise-server@3.17/admin/github-actions/managing-access-to-actions-from-githubcom/enabling-automatic-access-to-githubcom-actions-using-github-connect"
---

- [x] GitHub Connect を使用する
> 有効化すると、GitHub Connect を使用して GitHub Enterprise Server (GHES) インスタンスと GitHub Enterprise Cloud (GHEC) アカウント（GHEC は GitHub.com 上でホストされています）の間に安全な接続が自動的に確立されます。GHEC アカウントは、GitHub.com が GHES インスタンスに GitHub.com ホストの Actions へのアクセスを認可するために使用する信頼できる（認証済みの）ID として機能します。
- [ ] GitHub Enterprise Server はデフォルトで全ての GitHub.com Actions にアクセスできる
> GitHub Enterprise Server 上の GitHub Actions は、インターネットへの完全なアクセス権がない環境でも動作するよう設計されています。デフォルトでは、ワークフローは GitHub.com や GitHub Marketplace の Actions を使用することはできません。
- [ ] actions-sync ツールを使用する
> actions-sync を使用して、GitHub.com からエンタープライズに個々のアクションリポジトリを同期することはできますが、これは手動アプローチです。詳細については、[ドキュメント](https://docs.github.com/ja/enterprise-server@3.17/admin/github-actions/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom#about-the-actions-sync-tool)を参照してください。
- [ ] GitHub Enterprise Server (GHES) はオンプレミスの性質上、GitHub.com Actions を使用できず、インターネットアクセスがありません。
> GHES インスタンス上にあるワークフローは、デフォルトでは GitHub.com Actions および GitHub Marketplace Actions を使用することはできませんが、GitHub Connect や actions-sync を使用することで解決可能です。
