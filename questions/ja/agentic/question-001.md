---
question: "GitHub Copilotのカスタムエージェントプロファイルで、エージェントがアクセスできるMCPサーバーを宣言するために使用されるトップレベルのYAMLフロントマターキーはどれですか？"
documentation: "https://docs.github.com/en/copilot/reference/custom-agents-configuration"
---

- [x] `mcp-servers`
> `mcp-servers`キーは、タイプ、コマンド、引数、ツール、環境変数を含むMCPサーバーの設定を定義します。
- [ ] `tools`
> `tools`はエージェントが使用できるツールを列挙しますが、MCPサーバーの設定自体は定義しません。
- [ ] `servers`
> カスタムエージェントのYAMLスキーマには`servers`キーは存在しません。
- [ ] `extensions`
> `extensions`はカスタムエージェントプロファイルのフロントマターで有効なキーではありません。
