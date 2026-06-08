---
question: "Como executar scripts personalizados em JavaScript diretamente em um workflow do GitHub Actions?"
documentation: "https://github.com/marketplace/actions/github-script"
---

- [x] Por meio da ação `actions/github-script`
> `actions/github-script` permite que você escreva e utilize JavaScript inline para fazer chamadas de API e acessar o contexto do workflow. Para usar `actions/github-script`, você o chama como qualquer outra ação, conforme descrito na [documentação](https://github.com/actions/github-script)
- [ ] Habilitando a configuração 'Permitir scripts personalizados em JavaScript' nas configurações de Actions de um repositório
> Não existe a configuração 'Permitir scripts personalizados em JavaScript' nas configurações de Actions de um repositório.
- [ ] Habilitando a configuração 'Permitir scripts personalizados em JavaScript' nas configurações de Actions de uma organização
> Não existe a configuração 'Permitir scripts personalizados em JavaScript' nas configurações de Actions de um repositório. Embora você possa ter que habilitar configurações como 'Permitir ações criadas pelo GitHub' nas configurações de Actions de uma organização para usar ações oficiais do GitHub, isso não está relacionado apenas ao `actions/github-script`.
- [ ] Escrevendo o conteúdo de um bloco de script na variável ambiental `GITHUB_SCRIPT`
> `GITHUB_SCRIPT` não é uma variável ambiental padrão do GitHub Actions. Uma lista de variáveis ambientais padrão pode ser encontrada na [documentação](https://docs.github.com/en/actions/reference/workflows-and-actions/variables)
- [ ] Em uma Ação JavaScript, defina a chave `using` como `'github-script'`
> Ações JavaScript devem ter a chave `using` definida como `node*`, onde `*` é uma versão suportada do Node.js. Geralmente, Ações JavaScript não precisam de `actions/github-script`.
