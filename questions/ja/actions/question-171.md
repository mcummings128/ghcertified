---
question: "ワークフローを再実行するのと新しいワークフローの実行を生成するのでは、なぜ異なるのですか？"
documentation: "https://docs.github.com/en/actions/how-tos/manage-workflow-runs/re-run-workflows-and-jobs"
---

- [x] ワークフローを再実行すると、失敗したワークフロージョブのみを再実行できますが、新しい実行を生成するとすべてのジョブが実行されます。
- [x] ワークフローを再実行すると、ジョブをトリガーした元のイベントのコミットSHAとGitリファレンスのコンテキスト内でワークフロージョブが実行されます。
- [x] ワークフローを再実行すると、選択したジョブに対して追加のデバッグログを有効にできます。
- [ ] ワークフローを再実行すると、`GITHUB_TRIGGERING_ACTOR` が変更されず、ワークフローを最初にトリガーした人物が明確になります。
> [ドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context)によると、`GITHUB_TRIGGERING_ACTOR` の値はワークフローを再実行した人物に基づいて更新されます。
- [ ] ワークフローを再実行すると、`GITHUB_ACTOR` が更新され、ワークフローを再実行した人物が明確になります。
> [ドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context)によると、`GITHUB_ACTOR` の値はワークフローを最初にトリガーした人物です。ワークフローを再実行しても変更されません。
- [ ] ワークフローを再実行すると、失敗したジョブ実行が上書きされ、実行がより簡潔に見えます。
> ジョブを再実行しても、失敗したジョブ実行は保持されます。UIを使用すると、元のジョブ実行とその後の再実行の間を簡単に切り替えることができます。  
