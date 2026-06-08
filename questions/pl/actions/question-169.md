---
question: "Manuela konfiguruje runnersy hostowane samodzielnie dla swojej organizacji, która ma mocno ograniczoną komunikację z adresami IP. Jak może zapewnić, że runnersy hostowane samodzielnie będą mogły komunikować się z GitHubem?"
documentation: "https://docs.github.com/en/enterprise-cloud@latest/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/managing-allowed-ip-addresses-for-your-organization#using-github-actions-with-an-ip-allow-list"
---

- [x] Dodanie adresu(-ów) IP runnersów hostowanych samodzielnie do listy dozwolonych adresów IP organizacji
> Runnersy hostowane samodzielnie komunikują się z GitHubem w celu wykonania różnych działań, jak pokazano w [dokumentacji](https://docs.github.com/en/enterprise-cloud@latest/actions/reference/runners/self-hosted-runners#communication). Aby umożliwić tę komunikację, należy dodać adres(-y) IP runnersa hostowanego samodzielnie do listy dozwolonych adresów IP
- [ ] Dodanie systemu operacyjnego runnersów hostowanych samodzielnie do listy dozwolonych systemów operacyjnych organizacji
- [ ] Dodanie pliku `.ip-exception` do najważniejszego poziomu struktury katalogów runnersa hostowanego samodzielnie
- [ ] Przejście na standardowe runnersy hostowane przez GitHub, ponieważ runnersy hostowane samodzielnie będą blokowane, jeśli włączone są listy dozwolonych adresów IP
- [ ] Wybranie pola wyboru „Allow access from self-hosted runners” w ustawieniach listy dozwolonych adresów IP organizacji
