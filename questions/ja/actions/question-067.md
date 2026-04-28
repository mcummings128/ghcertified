---
question: "ジョブを、構成変数 `MY_VAR` が `MY_VALUE` の値を持つ場合にのみトリガーする正しい方法はどれですか？"
documentation: "https://docs.github.com/en/actions/learn-github-actions/contexts#example-usage-of-the-vars-context"
---

- [x] ジョブレベルで以下の条件式を作成する方法
```yaml
my-job:
  if: ${{ vars.MY_VAR == 'MY_VALUE' }}
```
- [ ] ジョブレベルで以下の条件式を作成する方法
```yaml
my-job:
  if: ${{ vars.MY_VAR }} == 'MY_VALUE'
```
> 不正解です。`${{ }}`内では `vars.MY_VAR` のみ評価されます。この結果、`some_value == 'MY_VALUE'` のようなテキストとなり、GitHubはその非空文字列を比較の代わりに真として扱います  
> 詳細は https://docs.github.com/en/actions/reference/workflows-and-actions/expressions#literals を参照してください
- [ ] 構成変数は `if` 条件式で使用できないため不可能です
> それは `secrets` には当てはまりますが、構成変数には該当しません
- [ ] 構成変数はジョブレベルの `if` 条件式で使用できないため不可能です
> それは `secrets` には当てはまりますが、構成変数には該当しません
