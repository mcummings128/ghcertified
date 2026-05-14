---
question: "GitHub CLI のどのコマンドが、新しい Copilot クラウドエージェントセッションを開始し、自律的にタスクに取り組むことができますか？"
documentation: "https://docs.github.com/en/copilot/how-tos/use-copilot-agents/cloud-agent/create-a-pr"
---

- [x] `gh agent-task create`
> `gh agent-task create`（GitHub CLI v2.80.0+ が必要）は、ブランチや Pull Request を作成できるクラウドエージェントセッションを開始します。
- [ ] `gh copilot agent start`
> このコマンドは GitHub CLI には存在しません。
- [ ] `gh workflow run copilot-agent`
> これは GitHub Actions ワークフローを実行するものであり、Copilot クラウドエージェントセッションを開始するものではありません。
- [ ] `gh issue assign --copilot`
> API を使用して Copilot に Issue を割り当てることはできますが、これは正しい CLI コマンドの構文ではありません。
