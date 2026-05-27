---
question: "Por que você deveria usar OIDC ao conectar um workflow a provedores de nuvem?"
documentation: "https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/about-security-hardening-with-openid-connect"
---

- [x] OIDC evita que você precise manter credenciais de nuvem como segredos de longa duração no GitHub 
- [x] OIDC envolve a geração e uso de tokens de curta duração, o que é mais seguro
- [ ] Provedores de nuvem exigem o uso de OIDC.
> OIDC é opcional e recomendado, mas não estritamente exigido.
- [ ] Usar OIDC permite que você contorne a configuração de políticas de confiança com os provedores de nuvem
> Você deve configurar políticas de confiança com o provedor de nuvem para poder usar OIDC
- [ ] OIDC gera tokens JSON web (JWTs) que podem ser usados em diferentes jobs de workflow
> A infraestrutura do OIDC envolve a criação de JWTs que são únicos para cada job de workflow
- [ ] Usar OIDC em um workflow automaticamente salvará os logs daquele workflow no armazenamento em nuvem
> OIDC está relacionado à segurança ao conectar-se a provedores de nuvem, não ao armazenamento. Portanto, não está envolvido em salvar logs de workflows em nenhum lugar.
