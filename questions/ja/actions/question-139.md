---
question: "ランナーディアグノスティックロギングを有効にする方法は？"
documentation: "https://docs.github.com/en/actions/how-tos/monitor-workflows/enable-debug-logging#enabling-runner-diagnostic-logging"
---

- [x] `ACTIONS_RUNNER_DEBUG`という名前のシークレットまたは変数を`true`に設定する  
> 注記: `ACTIONS_RUNNER_DEBUG`は、OrganizationレベルまたはRepositoryレベルでシークレットまたは変数として設定できます。
- [x] `Enable debug logging enabled`を使用してワークフローを再実行する
- [ ] ワークフローのRepositoryに`ACTIONS_RUNNER_DEBUG`というトップレベルのフォルダを追加する
- [ ] 使用中のセルフホスト型ランナーの`_diag`ディレクトリに`runner-diagnostic-logs`というサブフォルダを追加する  
> `runner-diagnostic-logs`は、`ACTIONS_RUNNER_DEBUG`が有効化されたときにGitHubが生成するフォルダの名前です。混乱を避けるため、この名前のフォルダを他の場所に作成すべきではありません。
- [ ] セルフホスト型ランナーの`_diag`ディレクトリを`runner-diagnostic-logs`にリネームする  
> `_diag`ディレクトリをリネームすると、ロギングの動作に悪影響を及ぼす可能性があるため、絶対に行わないでください。
