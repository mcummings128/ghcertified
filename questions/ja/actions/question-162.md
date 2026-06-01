---
question: "メルセデスは、自分が作成したDockerコンテナアクションをGitHub Actions Marketplaceに公開したいと考えています。最低限必要なファイルは何ですか？"
documentation: "https://docs.github.com/en/actions/how-tos/create-and-publish-actions/publish-in-github-marketplace"
---

- [x] `action.yml`
> `action.yml`ファイルは、タイプに関係なくMarketplaceにアクションを公開するために必要です。
- [x] ワークフロー実行中にアクションの一部としてイメージがビルドされる場合の`Dockerfile`
> Dockerコンテナアクションは、イメージを最初から作成しなければならず、イメージレジストリから取得できない場合にのみ`Dockerfile`が必要です。`action.yml`内の`runs.image`の値は`Dockerfile`へのパスである必要があります。
- [ ] イメージをイメージレジストリから参照する場合の`Dockerfile`
> イメージレジストリ内のイメージを参照する場合、`Dockerfile`は必要ありません。`action.yml`の`runs.image`キーの値は、イメージ名に続いて`docker://`を付ける必要があります。詳細は、「runs」および「runs.image」セクションを[ドキュメント](https://docs.github.com/en/actions/reference/workflows-and-actions/metadata-syntax#runsimage)で確認してください。
- [ ] `README.md`
> `README.md`ファイルは、Marketplaceに公開されるアクションにGitHubが推奨しているものの、厳密な要件ではありません。
- [ ] `.dockerignore`
- [ ] `CONTRIBUTING.md`
