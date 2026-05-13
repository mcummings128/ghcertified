---
question: "`GITHUB_STEP_SUMMARY`に書き込むとどうなりますか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-commands#adding-a-job-summary"
---

```yaml
- name: "テストスイートの結果を記述"
  run: |
    echo "The results of the testing suite are:" >> $GITHUB_STEP_SUMMARY
```
- [x] この行をジョブサマリーに追加する
> `GITHUB_STEP_SUMMARY`に書き込むとジョブサマリーに追加され、ワークフローログの簡易版として利用できます。
- [ ] この行をGitHub Actions UIのステップ名のサブタイトルとして追加する
- [ ] この行を組み込みのアーティファクト`github-steps-summary.md`に追加する
- [ ] この行をステップレベルのデバッグメッセージとして出力する
> ステップでデバッグメッセージを出力するには、`::debug::`構文を使用する必要があります。リンクされたドキュメントの「デバッグメッセージの設定」セクションを参照してください。
