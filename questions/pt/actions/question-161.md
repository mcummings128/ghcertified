---
question: "Como os workflows se integram com o OIDC após o estabelecimento de uma relação de confiança?"
documentation: "https://docs.github.com/en/actions/concepts/security/openid-connect#how-oidc-integrates-with-github-actions"
---

- [x] Um trabalho do workflow solicita um token OIDC do provedor OIDC do GitHub. O token OIDC é então validado pelo provedor de nuvem, que fornece um token de acesso à nuvem para que o workflow possa acessar os recursos na nuvem.
- [ ] Um trabalho do workflow solicita um token de acesso à nuvem do provedor de acesso à nuvem do GitHub. O token é então validado pelo provedor de nuvem, que fornece um token OIDC para que o workflow possa acessar os recursos na nuvem.
> Os tokens OIDC são solicitados primeiro, e então um token de acesso à nuvem é gerado. Tokens OIDC não podem acessar recursos na nuvem.
- [ ] O gatilho de evento `on: OIDC_request` solicita um token de acesso à nuvem do provedor de acesso à nuvem do GitHub. O token é então validado pelo provedor de nuvem, permitindo que o workflow acesse os recursos na nuvem.
> Não existe gatilho de evento `on: OIDC_request`.
- [ ] O gatilho de evento `on: OIDC_request` solicita um token OIDC do provedor OIDC do GitHub. O token é então validado pelo provedor de nuvem, permitindo que o workflow acesse os recursos na nuvem.
> Não existe gatilho de evento `on: OIDC_request`.
- [ ] Após adicionar um workflow à lista de "workflows permitidos pelo OIDC" nas configurações do repositório, os workflows irão automaticamente criar tokens OIDC e de acesso à nuvem em seu próprio nome. Esses tokens podem então ser usados imediatamente no workflow para interagir com os provedores de nuvem.
> Não existe uma configuração "workflows permitidos pelo OIDC".  
