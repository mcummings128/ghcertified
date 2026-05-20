---
question: "どのような方法でワークフロー成果物を削除できますか？"
documentation: "https://docs.github.com/en/actions/how-tos/manage-workflow-runs/remove-workflow-artifacts"
---

- [x] GitHub ActionsのUIを使用して、ワークフロー実行に移動し、成果物を個別に削除する
- [x] GitHub ActionsのUIを使用して、成果物を生成したワークフロー実行自体を削除する
> ワークフロー実行を削除すると、その実行に関連付けられた成果物も削除されます。
- [x] 特定のGitHub APIエンドポイントを使用する
> GitHub APIには「成果物を削除する」エンドポイントがあります。詳細は[ドキュメント](https://docs.github.com/en/rest/actions/artifacts?apiVersion=2026-03-10#delete-an-artifact)をご参照ください。
- [ ] ワークフロー内で`actions/delete-artifact`アクションを使用する
- [ ] 自己ホストランナーにSSHでリモートアクセスし、`.github/artifacts`ディレクトリに移動して選択した成果物を削除する
> 成果物は通常、GitHubインフラストラクチャで保存されており、ランナーでは保存されません。
- [ ] 成果物の保持期間を0日に設定する
> 成果物の保持期間を0日に設定することはできません。詳細は[ドキュメント](https://docs.github.com/en/organizations/managing-organization-settings/configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-organization)をご参照ください。
