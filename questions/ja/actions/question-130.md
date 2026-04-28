---
question: "ワークフローレベルとジョブレベルの`outputs`ブロックに関して、以下のうち正しいものはどれですか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#example-defining-outputs-for-a-job"
---

- [ ] ジョブレベルの`outputs`ブロックは、呼び出し元ワークフローでのみ使用され、再利用可能なワークフローでは使用されるべきではありません。
> 再利用可能なワークフローには、ジョブレベルとワークフローレベルの両方の`outputs`ブロックを含めることができます。
- [x] ワークフローレベルの`outputs`ブロックは、再利用可能なワークフローでのみ使用され、呼び出し元ワークフローでは使用されるべきではありません。
> 「ワークフローレベル」の`outputs`ブロックは、再利用可能なワークフロー内で`workflow_call`の直下にある`outputs`ブロックを指します。再利用可能でないワークフローでは、`outputs`ブロックはジョブレベルでのみ存在すべきです。
- [x] 再利用可能なワークフローには、ワークフローレベルとジョブレベルの両方の`outputs`ブロックを含めることができます。
> 再利用可能なワークフローで出力を設定し、その同じ出力を呼び出し元ワークフローに渡したい場合、ワークフローレベルとジョブレベルの両方の`outputs`ブロックを使用する必要があります。
> 詳細については、ドキュメントを参照してください: https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows#using-outputs-from-a-reusable-workflow
- [ ] ジョブレベルの`outputs`ブロックは、次のような構造を持つ必要があります:
```
outputs:
    <output-name>
        value: ${{ steps.<step-name>.outputs.<output-name> }}
```
> ジョブレベルの`outputs`ブロックでは、`key=value`ペアの非ネスト構造が使用されます。詳細については、公式ドキュメント（https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#example-defining-outputs-for-a-job）を参照してください。
- [x] ワークフローレベルの`outputs`ブロックは、次のような構造を持つ必要があります:
```
outputs:
    <output-name>
        value: ${{ jobs.<job-name>.outputs.<output-name> }}
```
> ワークフローレベルの`outputs`ブロックは、上記の構造に従う必要があります。`value`キーは常に必要です。また、オプションで`description`キーを使用することもできます（上記の例には記載されていません）。  
> 詳細については、ドキュメントを参照してください - https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows#using-outputs-from-a-reusable-workflow
