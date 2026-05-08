---
question: "組織がストレージの懸念を理由に、保存されているアーティファクトの保持期間を短縮したいと考えています。これを組織レベルで行うにはどうすればよいですか？"
documentation: "https://docs.github.com/en/organizations/managing-organization-settings/configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-organization"
---

- [x] 組織のActions設定に移動し、「アーティファクトとログの保持」設定の値を編集する
- [ ] セルフホストランナーを使用し、`.github/retention-policy.yml`ファイルを作成し、`artifact-retention-period`キーの値を指定する
> アーティファクトの保持期間をカスタマイズすることはセルフホストランナーに限定されません。  
- [ ] 組織レベルで行うことはできません。`actions/upload-artifact`を利用するすべてのワークフローは、必須の`retention-days`入力を使用する必要があります。
> `retention-days`入力を使用してワークフローで作成された個々のアーティファクトの保持期間をカスタマイズすることは可能ですが、これは組織レベルの包括的なポリシーを適用する場合には不適切です。さらに、`retention-days`入力は[必須ではなくオプションです](https://github.com/actions/upload-artifact#inputs)。
- [ ] これは行えません：アーティファクトはGitHub Actionsを実装しているすべてのシステムで厳密に90日間保存されます。
> アーティファクトのデフォルトの保持期間は90日です。この値をGitHub Actionsを実装しているすべてのシステムで変更することが可能です。
