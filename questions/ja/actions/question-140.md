---
question: "再利用可能なワークフローを作成しており、`branch-name`を入力として使用しています。このワークフロー内で、ブランチ名が'smoke-test'で始まる場合に、ステップを条件付きで実行するにはどうすればよいですか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/expressions#startswith"
---

- [x] 組み込みメソッド`startsWith`を`jobs.<job_id>.steps[*].if`と組み合わせて使用する
```yaml
    if: startsWith(inputs.branch-name, 'smoke-test')
```

- [ ] 組み込みメソッド`startsWith`を`jobs.<job_id>.steps[*].if`と組み合わせて使用する
```yaml
    if: inputs.branch-name.startsWith('smoke-test')
``` 
> GitHub Actionsの組み込みメソッドではメソッドチェーンを使用できません。ほとんどすべての組み込みメソッドは`methodName(arg1,arg2,...)`の形式で記述されます。
- [ ] `workflow_call`の`branches`フィルタを使用する
```yaml
on:
  workflow_call:
    branches:
        - 'smoke-test/**'
```
> `branches`フィルタは`workflow_call`イベントトリガーでは使用できません。さらに、ワークフローイベントトリガーはステップの実行制御には使用できません。

- [ ] シェル条件式を`jobs.<job_id>.steps[*].if`と組み合わせて使用する
```yaml
    if: [[ "${{inputs.branch-name}}" == "smoke-test"* ]]
```
> `jobs.<job_id>.steps[*].if`条件式では、GitHub Actionsでサポートされているコンテキストと式のみが使用できます。
