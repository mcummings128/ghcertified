---
question: "あなたのワークフローは、毎週月曜日と金曜日の午前12時にトリガーされる必要があります。次のスニペットのうち、この動作に対応するものはどれですか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#schedule"
---

- [x] 
```yaml
on:
  schedule:
    - cron: '0 0 * * 1,5'
```
> `cron`構文では、アイテムが大きさの順に定義されていますが、「曜日」アイテムは最後の項目です。詳細と例については、[ドキュメント](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/crontab.html#tag_20_25_07)をご覧ください。

- [ ] 
```yaml
on:
  schedule:
    - cron: '0 12 * * Mon,Fri'
```
> 「曜日」アイテムは数値形式で指定する必要があります。また、「分」と「時間」のアイテムは午前12時ではなく午後12時を指しています。

- [ ] 
```yaml
on:
  workflow_schedule:
    - cron: '0 0 * * 1,5'
```

- [ ] 
```yaml
on:
  workflow_schedule:
    - cron: '1,5 * * 0 0'
```

- [ ] 
```yaml
on:
  workflow_call:
    - days: [Mon,Fri]
    - times: [00]
```
