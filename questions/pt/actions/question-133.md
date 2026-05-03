---
question: "Por que usar um SHA de commit em vez de uma tag para fixar uma ação?"
documentation: "https://docs.github.com/en/actions/reference/security/secure-use#using-third-party-actions"
---

- [x] SHAs de commit são mais seguros
> SHAs de commit são mais seguros porque atualmente são a única maneira de usar uma ação como uma versão imutável.
- [x] SHAs de commit são imutáveis, enquanto as tags têm potencial para serem alteradas
> [Tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging) apontam para commits específicos. Sua referência pode ser alterada, o que nem sempre é óbvio. Vulnerabilidades relacionadas a tags podem ser mitigadas ativando [versões imutáveis](https://docs.github.com/en/code-security/concepts/supply-chain-security/immutable-releases), mas um SHA de commit sempre aponta para o mesmo commit e é imutável.
> Reexecutar um workflow usa o mesmo SHA de commit e referência Git do evento original que acionou a execução do workflow.
- [ ] SHAs de commit são mais convenientes de usar em comparação às tags
> Embora mais seguras, as tags geralmente são mais fáceis de usar.
- [x] SHAs de commit garantem apontar para exatamente o mesmo código todas as vezes, ao contrário das tags
- [ ] SHAs de commit são mais difíceis de rastrear em uma auditoria, dificultando que agentes mal-intencionados determinem como o código de uma ação se encaixa nos processos gerais.
> Os SHAs de commit sempre apontam para o mesmo commit. Ao fixar uma ação a um SHA, o SHA é explicitamente referenciado, o que significa que você pode encontrar o commit correspondente no repositório da ação. Esses fatores tornam a auditoria mais fácil.
> As tags podem ter suas referências alteradas, e isso nem sempre é óbvio. Isso pode resultar em cenários confusos quando a tag aponta para um novo commit, porque o código que faz referência à ação não parece ter mudado. Assim, em cenários de auditoria, você terá que descobrir para qual commit a tag estava apontando e para qual ela está apontando atualmente.
