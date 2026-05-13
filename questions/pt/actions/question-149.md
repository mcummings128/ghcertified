---
question: "O que escrever em `GITHUB_STEP_SUMMARY` faz?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-commands#adding-a-job-summary"
---

```yaml
- name: "Escrever resultados da suíte de testes"
  run: |
    echo "Os resultados da suíte de testes são:" >> $GITHUB_STEP_SUMMARY
```
- [x] Adiciona esta linha ao resumo do trabalho
> Escrever em `GITHUB_STEP_SUMMARY` adiciona ao resumo do trabalho, que pode ser usado como uma versão simplificada de um log de fluxo de trabalho.
- [ ] Adiciona esta linha como um subtítulo ao nome da etapa na interface do GitHub Actions
- [ ] Adiciona esta linha ao artefato embutido `github-steps-summary.md`
- [ ] Imprime esta linha como uma mensagem de depuração no nível da etapa
> Para imprimir uma mensagem de depuração em uma etapa, você deve usar a sintaxe `::debug::`. Consulte a seção "Setting a debug message" na documentação vinculada.
