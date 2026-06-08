---
question: "Por que você executaria novamente um workflow em vez de gerar uma nova execução de workflow?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-workflow-runs/re-run-workflows-and-jobs"
---

- [x] Executar novamente um workflow permite reexecutar os jobs de workflow que falharam, ao contrário de gerar uma nova execução, que executará todos os jobs.
- [x] Executar novamente um workflow significa que os jobs de workflow são executados no mesmo contexto do commit SHA e da referência git do evento original que acionou o job.
- [x] Executar novamente um workflow permite habilitar registro adicional de depuração para os job(s) selecionados.
- [ ] Executar novamente um workflow garante que `GITHUB_TRIGGERING_ACTOR` permaneça inalterado, de forma que não haja ambiguidade sobre quem originalmente acionou o workflow.
> Conforme a [documentação](https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context), o valor de `GITHUB_TRIGGERING_ACTOR` é atualizado com base em quem executou novamente o workflow.  
- [ ] Executar novamente um workflow garante que `GITHUB_ACTOR` seja atualizado, de forma que não haja ambiguidade sobre quem executou novamente o workflow.
> Conforme a [documentação](https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context), o valor de `GITHUB_ACTOR` é quem originalmente acionou o workflow; ele não muda ao reexecutar um workflow.
- [ ] Executar novamente um workflow substitui as execuções de jobs com falhas, tornando as execuções mais simples.
> As execuções de jobs com falhas permanecem quando um job é reexecutado. Usando a interface gráfica, é fácil alternar entre a execução original do job e as reexecuções subsequentes.  
