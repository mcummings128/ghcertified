---
question: "次のワークフローでは、ジョブの1つで再利用可能なワークフローを呼び出しています。再利用可能なワークフローには、以下のようにワークフローのレベルで`permissions`が定義されています。この再利用可能なワークフローを呼び出した結果はどうなりますか？"
documentation: "https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows"
---

```yaml
# 呼び出し元ワークフロー
on:
    issues:
        types: [opened]
    
    permissions:
        contents: write

    jobs:
        issue_creator:
            permissions:
                contents: read
            uses: ./.github/workflows/issue-creator.yml

# 再利用可能なワークフロー (issue-creator.yml)
on:
    workflow_call:

    permissions:
        contents: write

    jobs:
        create_issue:
            runs-on: ubuntu-latest
            steps: 
                env: GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}    
                - run: gh issue create --title "Issue report" --body "Hello!" --repo $GITHUB_REPOSITORY

```
- [x] 再利用可能なワークフローはエラーを返します。これは、呼び出し元のジョブに`contents:read`の権限しかないためです。
> このシナリオでは、呼び出し元ワークフローはトリガーされますが、そのジョブは実行されません。代わりにエラーが生成され、「呼び出し元ワークフローファイルが無効である」と表示されます。これは、再利用可能なワークフローが`contents:write`を要求していますが、呼び出し元で許可されていないためです。
- [ ] 再利用可能なワークフローは、リポジトリにタイトルが`"Issue Report"`のIssueを作成します。
> これは、`issue_creator`ジョブが`contents:write`権限を持っている場合に発生します。この場合、再利用可能なワークフローがその権限を引き継ぎます。
- [ ] 再利用可能なワークフローは呼び出されません。再利用可能なワークフローは`.github/workflows`のサブフォルダー内になければならないからです。
> すべてのワークフローは`.github/workflows`ディレクトリに配置する必要があります。
- [ ] 呼び出し元および再利用可能な両方のワークフローは呼び出されません。なぜなら、`issues`はGitHub Actionsで使用可能なトリガーではないからです。
> `issues`は標準的なイベントトリガーです。[ドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#issues)で確認できます。
