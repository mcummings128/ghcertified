---
question: "空欄を埋めてください: セルフホストランナーを使用する場合、ツールキャッシュは ___"
documentation: "https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/setting-up-the-tool-cache-on-self-hosted-runners-without-internet-access"
---

- [x] 初期状態では空であり、ランの間にツールを保存するためにデータを追加する必要があります
> ツールキャッシュを使用すると、さまざまなバージョンのツールをキャッシュできるため、セルフホストランナーの処理速度が向上します。ツールキャッシュがない場合、`actions/setup-*` を使用するセルフホストランナーの実行時間が長くなります。
- [ ] GitHubホストランナーと同様に、特定のツールがあらかじめ設定された状態で開始します
> GitHubホストランナーには特定のツールが事前にインストールされていますが、セルフホストランナーではそうではありません。
- [ ] GitHubホストランナーと同じツール、およびセルフホストランナー管理を強化するためのカスタムツールの選定セットで開始します
- [ ] データを追加できません
