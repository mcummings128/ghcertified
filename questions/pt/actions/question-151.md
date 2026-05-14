---
question: "Qual você deve usar ao passar informações entre jobs: saídas de jobs ou `GITHUB_ENV`?"
documentation: "https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/use-variables#passing-values-between-steps-and-jobs-in-a-workflow"
---

- [x] Saídas de jobs, porque o valor das variáveis de ambiente definidas escrevendo no `GITHUB_ENV` só se aplica ao job atual.
> Embora `env` possa ser definido no nível do workflow (o que significa que suas variáveis podem ser referenciadas por vários jobs), isso não significa que alterar o valor da variável de ambiente persista além do job que a alterou.
- [ ] `GITHUB_ENV`, porque as saídas de jobs só podem ser definidas e referenciadas dentro do mesmo job.
- [ ] Saídas de jobs, porque são mais simples de configurar.
> Configurar e referenciar saídas de jobs é mais complicado do que utilizar `GITHUB_ENV`. Por exemplo, saídas de jobs exigem configurar um bloco de `outputs`, adicionar um `id` a um passo e usar `needs` para indicar dependências.
- [ ] `GITHUB_ENV`, porque usá-lo para definir variáveis de ambiente reduz significativamente a carga no runner, diminuindo o tempo de execução do workflow.
