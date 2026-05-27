---
question: "W jaki sposób workflow integruje się z OIDC po ustanowieniu zaufanej relacji?"
documentation: "https://docs.github.com/en/actions/concepts/security/openid-connect#how-oidc-integrates-with-github-actions"
---

- [x] Zadanie workflow żąda tokena OIDC od dostawcy OIDC GitHub. Token OIDC jest następnie weryfikowany przez dostawcę chmury, który dostarcza token dostępu do zasobów chmury, co umożliwia workflow dostęp do zasobów chmurowych.
- [ ] Zadanie workflow żąda tokena dostępu do chmury od dostawcy dostępu do chmury GitHub. Token jest następnie weryfikowany przez dostawcę chmury, który dostarcza token OIDC, co umożliwia workflow dostęp do zasobów chmurowych.
> Tokeny OIDC są żądane najpierw, a następnie generowany jest token dostępu do chmury. Tokeny OIDC nie mogą uzyskiwać dostępu do zasobów chmurowych.
- [ ] Wyzwalacz zdarzenia `on: OIDC_request` żąda tokena dostępu do chmury od dostawcy dostępu do chmury GitHub. Token jest następnie weryfikowany przez dostawcę chmury, co umożliwia workflow dostęp do zasobów chmurowych.
> Nie istnieje wyzwalacz zdarzenia `on: OIDC_request`.
- [ ] Wyzwalacz zdarzenia `on: OIDC_request` żąda tokena OIDC od dostawcy OIDC GitHub. Token jest następnie weryfikowany przez dostawcę chmury, co umożliwia workflow dostęp do zasobów chmurowych.
> Nie istnieje wyzwalacz zdarzenia `on: OIDC_request`.
- [ ] Po dodaniu workflow do listy "OIDC-allowed workflows" w ustawieniach repozytorium, workflow automatycznie tworzy tokeny OIDC i tokeny dostępu do chmury we własnym imieniu. Tokeny te mogą być następnie natychmiast wykorzystane w workflow do interakcji z dostawcami chmury.
> Nie istnieje ustawienie "OIDC-allowed workflows".
