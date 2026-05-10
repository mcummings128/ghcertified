---
question: "どのような方法でアーティファクトをダウンロードできますか？"
documentation: "https://github.com/actions/upload-artifact#inputs"
---

- [x] ワークフロー内で`actions/download-artifact`アクションを使用する 
- [x] GitHub Actions UIのワークフロー実行からアーティファクトをダウンロードする  
> UIを使用すると、アーティファクトを手動でダウンロードすることができます。詳細は[ドキュメント](https://docs.github.com/en/actions/how-tos/manage-workflow-runs/download-workflow-artifacts)をご覧ください。
- [x] 特定のGitHub APIエンドポイントを使用する  
> GitHub APIには「アーティファクトをダウンロードする」エンドポイントがあります。詳細は[ドキュメント](https://docs.github.com/en/rest/actions/artifacts?apiVersion=2026-03-10#download-an-artifact)をご覧ください。
- [ ] ワークフロー内で`actions/upload-artifact`アクションを使用する  
> `actions/upload-artifact`はアーティファクトをアップロードするために使用され、ダウンロードには使用されません。
- [ ] リモートで自己ホスト型ランナーにSSH接続し、`.github/artifacts`ディレクトリにアクセスする  
> アーティファクトは通常、GitHubのインフラストラクチャを使用して保存されますが、例外があります。GitHub Enterprise Server (GHES)を使用している場合、ワークフロー実行で生成されたアーティファクトやその他のデータは、外部のBlobストレージに保存されます。GHESストレージの詳細については[ドキュメント](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/getting-started-with-github-actions-for-your-enterprise/getting-started-with-github-actions-for-github-enterprise-server#external-storage-requirements)をご覧ください。
