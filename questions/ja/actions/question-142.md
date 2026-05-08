---
question: "次の回答のうち、インストールアクセストークンに関して正しいものはどれですか？"
documentation: "https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/authenticating-as-a-github-app-installation#using-an-installation-access-token-to-authenticate-as-an-app-installation"
---

- [x] インストールアクセストークンは、短期間しか有効でないトークンであり、自動化活動に最適ですが、GitHub Appのセットアップが必要です。
- [x] `GITHUB_TOKEN` はインストールアクセストークンの一種です。
> `GITHUB_TOKEN` は GitHub App のインストールアクセストークンで、各ワークフロー実行時に自動生成されます。詳細については[ドキュメント](https://docs.github.com/en/actions/concepts/security/github_token)をご覧ください。
- [x] ワークフロー内で `actions/create-github-app-token` を呼び出して、即時利用可能なインストールアクセストークンを作成できます。
- [ ] ワークフロー内で `actions/create-github-app-token` を呼び出してインストールアクセストークンを作成できますが、そのインストールアクセストークンはワークフローの今後の実行でしか使用できません。
> 作成されたインストールアクセストークンは即時利用可能です。このアクションの詳細については[公式ページ](https://github.com/actions/create-github-app-token)をご覧ください。
- [ ] インストールアクセストークンは、関連するGitHub Appを代行するように設定することはできません。
> インストールアクセストークンは、多くの場合、関連するGitHub Appを代行するように設定されます。これにより、自動化活動の監査が容易になります。
