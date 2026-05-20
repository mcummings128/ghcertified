---
question: "GitHub Actions マーケットプレイスで共有するために Docker コンテナアクションを構築するのはいつですか？"
documentation: "https://docs.github.com/en/actions/concepts/workflows-and-actions/custom-actions#docker-container-actions"
---

- [x] Docker コンテナアクションは、一貫したランタイム環境と特定の依存関係を保証し、ユーザーがこれらの側面を自分で処理する必要がなくなります
- [ ] Docker コンテナアクションは、すぐに使える低オーバーヘッドのアクションです
> Docker コンテナアクションは、イメージ（事前に構築されたものや `Dockerfile` によって指定されたもの）、エントリーポイントスクリプト、場合によってはエントリーポイントの前後のロジックが必要なため、低オーバーヘッドとは見なされません。
- [ ] Docker コンテナアクションは、Windows および macOS ランナー上で高速に起動します
> Docker コンテナは Linux OS ランナー（GitHub ホストランナーの場合は `ubuntu-latest`）上でのみ実行可能です。また、JavaScript アクションやコンポジットアクションと比較して時間がかかります。
- [ ] Docker コンテナアクションは、呼び出し元のワークフロー/アクションのコンテキスト内で実行される他のワークフロー内のステップのバンドルです
> 「再利用可能なステップのバンドル」は、Docker コンテナアクションではなくコンポジットアクションを指します。
- [ ] Docker コンテナアクションは、`action.yml` ファイルを必要とせずに Docker を利用できます
> すべてのアクションは、タイプに関係なく `action.yml` ファイルを使用する必要があります。
