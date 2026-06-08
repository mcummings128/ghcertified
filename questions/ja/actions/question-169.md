---
question: "Manuelaは、IPアドレスとの通信が厳しく制限されている組織のためにセルフホストランナーを設定しています。セルフホストランナーがGitHubと通信できるようにするには、どうすればよいでしょうか？"
documentation: "https://docs.github.com/en/enterprise-cloud@latest/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/managing-allowed-ip-addresses-for-your-organization#using-github-actions-with-an-ip-allow-list"
---

- [x] 組織のIP許可リストにセルフホストランナーのIPアドレスを追加する
> セルフホストランナーはさまざまな活動を行うためにGitHubと通信します。これを許可するには、[ドキュメント](https://docs.github.com/en/enterprise-cloud@latest/actions/reference/runners/self-hosted-runners#communication)に記載されているように、セルフホストランナーのIPアドレスをIP許可リストに追加する必要があります。
- [ ] 組織のオペレーティングシステム許可リストにセルフホストランナーのオペレーティングシステムを追加する
- [ ] `.ip-exception`ファイルをセルフホストランナーのディレクトリ構造のトップレベルに追加する
- [ ] GitHubホストの標準ランナーに切り替える（IP許可リストが有効になっている場合、セルフホストランナーはブロックされるため）
- [ ] 組織のIP許可リスト設定で「セルフホストランナーからのアクセスを許可する」チェックボックスを選択する
