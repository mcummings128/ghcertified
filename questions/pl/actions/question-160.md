---
question: "Dlaczego warto używać OIDC podczas łączenia workflow z dostawcami chmury?"
documentation: "https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/about-security-hardening-with-openid-connect"
---

- [x] OIDC zapobiega konieczności przechowywania długoterminowych danych uwierzytelniających w postaci GitHub secrets 
- [x] OIDC obejmuje generowanie i używanie krótkoterminowych tokenów, co jest bardziej bezpieczne
- [ ] Dostawcy chmury wymagają użycia OIDC.
> OIDC jest opcjonalne i zalecane, ale nie jest bezwzględnie wymagane.
- [ ] Używanie OIDC pozwala obejść konfigurację zasad zaufania z dostawcami chmury
> Aby używać OIDC, musisz skonfigurować zasady zaufania z dostawcą chmury
- [ ] OIDC generuje JSON web tokeny (JWT), które mogą być używane w różnych zadaniach workflow
> Infrastruktura OIDC obejmuje tworzenie tokenów JWT unikalnych dla każdego zadania workflow
- [ ] Korzystanie z OIDC w ramach workflow automatycznie zapisuje logi tego workflow w pamięci chmury
> OIDC dotyczy bezpieczeństwa podczas łączenia z dostawcami chmury, a nie przechowywania danych. W związku z tym nie jest zaangażowane w zapisywanie logów workflow.
