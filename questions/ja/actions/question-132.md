---
question: "次のうち、GitHub Enterprise Server (GHES) に関して正しいものはどれですか？"
documentation: "https://docs.github.com/en/enterprise-server/admin/overview/about-github-enterprise-server"
---

- [x] GHES のワークフローは、デフォルトでは GitHub.com および GitHub Marketplace アクションにアクセスできません。 
- [x] `actions/actions-sync` は主に、GitHub.com のアクションを GHES インスタンスに移動することを目的としています。
> GitHub.com からアクションを同期する主な方法は、GitHub Connect または `actions-sync` を使用することです。`actions/actions-sync` ツールは、このプロセスを実行するための[手動の方法](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom)です。
- [ ] GHES は GitHub ホストランナーの拡張版を使用することが許可されています。
> GHES は GitHub ホストランナーに全くアクセスできません。この点は [`actions/actions-sync` のドキュメント](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom) に記載されています。
- [ ] GitHub Connect を使用すると、ユーザーは手動プロセスを経て GitHub.com のアクションにアクセスできます。このプロセスは必要な各アクションごとに一度行う必要があります。
> GitHub Connect を使用すると、GitHub.com のアクションに自動的にアクセスできます。ユーザーはセットアッププロセスを実行する必要がありますが、通常は一度設定するだけで済みます。詳細については、[GitHub Connect のドキュメント](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/enabling-automatic-access-to-githubcom-actions-using-github-connect#enabling-automatic-access-to-public-githubcom-actions)を参照してください。
- [x] GitHub Enterprise Server のインスタンスは自己ホスト型であり、一方 GitHub Enterprise Cloud (GHEC) は GitHub によってホストおよび管理されています。
> [GitHub Enterprise Server](https://docs.github.com/en/enterprise-server/admin/overview/about-github-enterprise-server) は、GitHub プラットフォームの自己ホスト型バージョンです。[GitHub Enterprise Cloud](https://docs.github.com/en/enterprise-cloud@latest/admin/overview/about-github-enterprise-cloud) のインスタンスは、GHE.com の専用サブドメインでホストされています。すべての GHE.com サブドメインは GitHub によってホストされています。
