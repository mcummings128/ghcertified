---
question: "組織には、プライベートネットワーク上でホストされる専門的な Node.js 環境を共有する複数のリポジトリがあります。組織の次の目標は、そのネットワーク内にノードロックソフトウェアを設定することです。ワークフローを実行する際に、組織のニーズに最も適した選択肢は次のうちどれですか？"
documentation: "https://docs.github.com/en/actions/concepts/runners/self-hosted-runners"
---

- [x] 組織レベルで設定された Self-hosted runners
- [ ] 各リポジトリごとに設定された Self-hosted runner
> これは重複的で管理が複雑になります。リポジトリは同じ組織レベルのランナーを参照でき、これがこの状況での正しいアプローチです。
- [ ] GitHub-hosted runners を使用し、すべてのワークフローで `actions/setup-node` を利用
> GitHub-hosted runners は[短命的](https://docs.github.com/en/actions/concepts/runners/github-hosted-runners#overview-of-github-hosted-runners)であり、ワークフローランごとに新しいランナーインスタンスが設定されます。これは、特定のデバイスやVMでのみソフトウェアが実行可能なノードロックソフトウェアには適していません。また、GitHub-hosted runners はプライベートネットワークへのアクセスを設定できますが、これはデフォルトの機能ではありません。
- [ ] 組織レベルで設定された GitHub-hosted runners
> GitHub-hosted runners はこのようには設定できません。
- [ ] GitHub-hosted runners を使用し、すべてのワークフローで `runs-on: [node<version>]`（`<version>` は希望する Node バージョン）を使用
> `[node<version>]` は GitHub-hosted runner を指しません。
