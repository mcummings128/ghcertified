---
question: "`GITHUB_TOKEN` może być używany do klonowania dowolnego repozytorium."
documentation: "https://docs.github.com/en/actions/concepts/security/github_token#about-the-github_token"
---

- [ ] Prawda
- [ ] Tylko z podwyższonymi uprawnieniami
- [x] Fałsz
> Uprawnienia `GITHUB_TOKEN` są ograniczone do repozytorium, które zawiera wyzwolony workflow. 
> Aby klonować inne repozytorium, należy użyć innych metod, takich jak token dostępu osobistego (PAT) lub token dostępu instalacji.
