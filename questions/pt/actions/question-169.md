---
question: "Manuela está configurando runners self-hosted para sua organização, que possui comunicação altamente restrita com endereços IP. Como ela pode garantir que os runners self-hosted possam se comunicar com o GitHub?"
documentation: "https://docs.github.com/en/enterprise-cloud@latest/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/managing-allowed-ip-addresses-for-your-organization#using-github-actions-with-an-ip-allow-list"
---

- [x] Adicionando os endereços IP dos runners self-hosted à lista de endereços IP permitidos da organização
> Os runners self-hosted comunicam-se com o GitHub para realizar diversas atividades, conforme descrito na [documentação](https://docs.github.com/en/enterprise-cloud@latest/actions/reference/runners/self-hosted-runners#communication). Para permitir essa comunicação, você deve adicionar os endereços IP dos runners self-hosted à lista de endereços IP permitidos
- [ ] Adicionando o sistema operacional dos runners self-hosted à lista de sistemas operacionais permitidos da organização
- [ ] Adicionando o arquivo `.ip-exception` no nível superior da estrutura de diretórios do runner self-hosted
- [ ] Mudando para runners padrão hospedados no GitHub, já que runners self-hosted serão bloqueados se listas de IPs permitidos estiverem ativadas
- [ ] Selecionando a caixa de seleção 'Permitir acesso de runners self-hosted' nas configurações da lista de endereços IP permitidos da organização
