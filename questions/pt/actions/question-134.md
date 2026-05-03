---
question: "Como executar scripts personalizados em JavaScript diretamente em um workflow do GitHub Actions?"
documentation: "https://github.com/marketplace/actions/github-script"
---

- [x] Através da action `actions/github-script`
> A action `actions/github-script` permite que você escreva e utilize JavaScript inline para realizar chamadas API e acessar o contexto do workflow. Para usar o `actions/github-script`, você o chama como qualquer outra action, conforme visto na [documentação](https://github.com/actions/github-script).
- [ ] Habilitando a configuração 'Allow custom JavaScript scripts' nas configurações de Actions de um repositório
> Não há uma configuração 'Allow custom JavaScript scripts' nas configurações de Actions de um repositório.
- [ ] Habilitando a configuração 'Allow custom JavaScript scripts' nas configurações de Actions de uma organização
> Não há uma configuração 'Allow custom JavaScript scripts' nas configurações de Actions de um repositório. Embora você possa precisar habilitar configurações como 'Allow actions created by Github' nas configurações de Actions de uma organização para usar as Actions oficiais do GitHub, isso não está apenas relacionado ao `actions/github-script`.
- [ ] Escrevendo o conteúdo de um bloco de script na variável de ambiente `GITHUB_SCRIPT`
> `GITHUB_SCRIPT` não é uma variável de ambiente padrão do GitHub Actions. Uma lista de variáveis de ambiente padrão pode ser encontrada na [documentação](https://docs.github.com/pt/actions/reference/workflows-and-actions/variables).
- [ ] Em uma Action JavaScript, defina a chave `using` como `'github-script'`
> Actions JavaScript devem ter sua chave `using` definida como `node*` onde * é uma versão suportada do Node.js. Geralmente, Actions JavaScript não têm a necessidade de `actions/github-script`.
