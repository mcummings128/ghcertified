---
question: "エンタープライズはどのようにしてGitHub Actionsの利用状況を追跡できますか？"
documentation: "https://docs.github.com/en/enterprise-cloud@latest/admin/github-actions/getting-started-with-github-actions-for-your-enterprise/introducing-github-actions-to-your-enterprise#tracking-usage"
---

- [x] Webhookを使用してワークフロージョブや実行に関する情報を購読し、データアーカイブシステムを利用することで追跡します。
- [x] 組織およびリポジトリレベルで利用可能なGitHub Actionsの使用状況およびパフォーマンスのメトリクスを使用します。
> GitHub Actionsのメトリクスは、組織およびリポジトリレベルのInsightsタブからアクセスでき、実行時間、キュー時間、失敗率などの使用状況およびパフォーマンスデータを提供します。
- [ ] 毎月末に各リポジトリのワークフロー実行およびジョブを手動でカウントすることによって追跡します。
- [ ] GitHub Actionsの使用状況は追跡できず、開発者のフィードバックをもとに推定する必要があります。
