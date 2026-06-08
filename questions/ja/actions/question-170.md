---
question: "以下のワークフロージョブに見られる `runs-on` キーの値について観察してください。このジョブの実行に関して正しいのはどれですか？"
documentation: "https://docs.github.com/en/actions/how-tos/manage-runners/self-hosted-runners/use-in-a-workflow#using-custom-labels-to-route-jobs"
---
```yaml
jobs:
    fire_emblem_deploy:
        name: "Deploy the 'Fire Emblem' application"
        runs-on: [self-hosted,nes,linux]
```

- [x] このジョブは、すべてのラベルが適用されたセルフホストランナーで実行されます。
- [ ] このジョブは、いずれかのラベルが適用されたセルフホストランナーで実行されます。
> ランナーラベルは累積的に適用されます。ワークフローは、一部のラベルのみを持つランナーでは実行されません。すべてのラベルが必要です。
- [ ] このジョブは、カスタムラベルを適用できるため、GitHubホストランナーでも実行できます。
> GitHubホストランナーにはカスタムラベルを適用できません。それらは、割り当てられた[事前定義のラベル](https://docs.github.com/en/enterprise-cloud@latest/actions/how-tos/write-workflows/choose-where-workflows-run/choose-the-runner-for-a-job#standard-github-hosted-runners-for-public-repositories)で参照する必要があります。
- [ ] このジョブは、名前が `self-hosted,nes,linux` というランナー（セルフホストまたはGitHubホスト、どちらでも最初に利用可能なもの）で実行されます。
> `runs-on` はランナー名ではなく、ランナーラベルを指します。
