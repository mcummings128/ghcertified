---
question: "Complete a lacuna: Ao usar runners auto-hospedados, o cache de ferramentas ___"
documentation: "https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/setting-up-the-tool-cache-on-self-hosted-runners-without-internet-access"
---

- [x] começa vazio e deve ser preenchido para salvar ferramentas entre as execuções
> Os caches de ferramentas permitem armazenar diferentes versões das ferramentas, o que possibilita uma atividade mais rápida dos runners auto-hospedados. Sem caches de ferramentas, os runners auto-hospedados que utilizam `actions/setup-*` levarão mais tempo para serem executados.
- [ ] começa igual aos runners hospedados pelo GitHub, sendo pré-preenchido com certas ferramentas
> Embora os runners hospedados pelo GitHub venham com certas ferramentas pré-instaladas, isso não se aplica aos runners auto-hospedados.
- [ ] começam com as mesmas ferramentas dos runners hospedados pelo GitHub, além de uma seleção de ferramentas personalizadas para aprimorar a gestão de runners auto-hospedados
- [ ] não podem ser preenchidos
