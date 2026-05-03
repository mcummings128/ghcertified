---
question: "Você tem um workflow que usa a matriz abaixo. Se um job na matriz falhar, como você pode garantir que outros jobs em andamento e na fila na matriz não sejam cancelados?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#jobsjob_idstrategyfail-fast"
---

```yaml
jobs:
  deploy:
    strategy:
      matrix:
        version: ["1", "1.2", "1.3"]
        os: [ubuntu-latest, windows-latest]
```

- [x] Defina `jobs.<job_id>.strategy.fail-fast` como `false`
> `jobs.<job_id>.strategy.fail-fast` está definido como `true` por padrão, o que significa que, se um job da matriz falhar, outros jobs em andamento e na fila serão cancelados. Você deve definir explicitamente `fail-fast` como `false` para evitar esse comportamento.
- [ ] Nada precisa ser feito, já que `jobs.<job_id>.strategy.fail-fast` tem configuração padrão como `false`
> `jobs.<job_id>.strategy.fail-fast` está definido como `true` por padrão.
- [ ] Defina `jobs.<job_id>.strategy.matrix.fail-fast` como `false`
> Isso está incorreto, `fail-fast` está no nível de `strategy`, não no nível de `matrix`. Se você definir `fail-fast` no nível de `matrix`, ele funcionará como parte da [configuração do job](https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/run-job-variations#adding-a-matrix-strategy-to-your-workflow-job) e não afetará o cancelamento/continuação de outros jobs da matriz.
- [ ] Nada precisa ser feito, já que `jobs.<job_id>.strategy.matrix.fail-fast` tem configuração padrão como `false`
> Isso está incorreto, `fail-fast` está no nível de `strategy`, não no nível de `matrix`.
- [ ] Não há como impor este comportamento, isso não pode ser contornado.
