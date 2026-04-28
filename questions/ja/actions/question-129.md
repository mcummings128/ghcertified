---
question: "`GITHUB_TOKEN` は任意のリポジトリをチェックアウトするために使用できます。"
documentation: "https://docs.github.com/en/actions/concepts/security/github_token#about-the-github_token"
---

- [ ] 正しい
- [ ] 権限が昇格された場合のみ
- [x] 誤り
> `GITHUB_TOKEN` の権限は、トリガーされたワークフローを含むリポジトリに限定されています。  
> 別のリポジトリをチェックアウトするには、個人アクセストークン（PAT）やインストールアクセストークンなど、他の方法で取得したトークンを使用する必要があります。
