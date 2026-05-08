---
question: "なぜ `actions/cache` を使用する際に `hashFiles` を使用するのでしょうか？"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/expressions#hashfiles"
---
```yaml
  - uses: actions/cache@v5
    with:
      path: ~/.npm
      key: ${{ runner.os }}-build-${{ env.cache-name }}-${{ hashFiles('**/package-lock.json') }}
```
- [x] キャッシュキーが依存関係ファイルを `hashFiles` でラップした場合、依存関係ファイルが更新されるとキーが変更され、それにより最新の状態を維持するのに役立ちます。
> `hashFiles` は指定されたパスのハッシュを作成するGitHubの組み込み関数です。これを利用してキャッシュキーを構成すると、ハッシュが再生成され、それによりキャッシュキーが更新されます。公式の[Dependency Caching Reference](https://docs.github.com/en/actions/reference/workflows-and-actions/dependency-caching#example-using-the-cache-action) ドキュメントでは、キャッシュキーの一部として `hashFiles` を使用する方法が示されています。
- [ ] `hashFiles` は、Windowsランナーとの互換性を保つために必要です。
- [ ] キャッシュキーの一部として `hashFiles` を使用すると、キャッシュミスが発生した場合に `hashFiles` が追加のデバッグ情報を提供します。  
- [ ] キャッシュキーの一部として `hashFiles` を使用すると、呼び出し元のワークフローに追加のステップが生成されます。このワークフローステップは、参照目的でキャッシュキーのSHA-256ハッシュ値を出力します。  
> キャッシュキーのハッシュを作成することは、ほとんどの場合有用ではありません。
