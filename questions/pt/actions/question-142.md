---
question: "Qual das opções a seguir está correta em relação aos tokens de acesso de instalação?"
documentation: "https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/authenticating-as-a-github-app-installation#using-an-installation-access-token-to-authenticate-as-an-app-installation"
---

- [x] Tokens de acesso de instalação são tokens de curta duração ideais para atividades de automação, mas requerem a configuração de um Github App.
- [x] `GITHUB_TOKEN` é um tipo de token de acesso de instalação.
> `GITHUB_TOKEN` é um token de acesso de instalação de GitHub App que é gerado automaticamente para cada execução de workflow. Consulte a [documentação](https://docs.github.com/en/actions/concepts/security/github_token) para mais detalhes.
- [x] A `actions/create-github-app-token` pode ser chamada dentro de workflows para criar um token de acesso de instalação disponível para uso imediato.
- [ ] A `actions/create-github-app-token` pode ser chamada dentro de workflows para criar um token de acesso de instalação, mas o token de acesso de instalação só pode ser usado em execuções futuras do workflow.
> Uma vez criado, um token de acesso de instalação pode ser usado imediatamente. Consulte a [página oficial desta ação](https://github.com/actions/create-github-app-token) para mais detalhes.
- [ ] Tokens de acesso de instalação não podem ser configurados para agir em nome do seu GitHub App associado.
> Tokens de acesso de instalação são frequentemente configurados para agir em nome do seu GitHub App associado. Isso pode ajudar na auditoria de atividades automatizadas.
