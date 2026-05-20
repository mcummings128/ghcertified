---
question: "Marianneは、自身の新しいworkflowファイルを含むfeatureブランチを持っており、以下の構文を使用して毎日午前2時にトリガーされるよう設定しています。しかし、翌日になってもworkflowが実行されません。この理由として考えられるのは何でしょうか？"
documentation: "https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule"
---

```yaml
on:
    schedule:
        cron:
            "0 2 * * *"
```

- [x] `schedule`イベントによってトリガーされるには、workflowファイルがデフォルトブランチ上に存在している必要があります
- [ ] `cron`構文のスケジュールが正しく設定されていません
> `"0 2 * * *"`はCRON構文において「毎日午前2時に実行」を意味します。スケジュールが誤って設定されていた場合であっても、workflowがデフォルトブランチ上に存在しない限りトリガーされません。
- [ ] `schedule`は単独ではworkflowイベントとして使用できません。`push`などのリポジトリベースのイベントと組み合わせる必要があります
- [ ] `@daily`構文が使用されていません
> `@daily`のような非標準のCRON構文はGitHub Actionsではサポートされていません。
- [ ] workflowを含むプライベートリポジトリが60日以上リポジトリアクティビティがないため、自動的に無効化されています。
> この自動無効化はプライベートリポジトリではなく、公開リポジトリでのみ発生します。
