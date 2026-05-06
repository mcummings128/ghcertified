---
question: "Quais são as maneiras de ativar o registro de diagnóstico do runner?"
documentation: "https://docs.github.com/en/actions/how-tos/monitor-workflows/enable-debug-logging#enabling-runner-diagnostic-logging"
---

- [x] Configurar um segredo ou variável chamada `ACTIONS_RUNNER_DEBUG` como `true`
> Nota: `ACTIONS_RUNNER_DEBUG` pode ser configurado como um segredo ou variável no nível da organização ou do repositório.
- [x] Reexecutar um workflow com `Enable debug logging enabled`
- [ ] Adicionando uma pasta de nível superior chamada `ACTIONS_RUNNER_DEBUG` ao repositório do workflow
- [ ] Adicionando uma subpasta `runner-diagnostic-logs` ao diretório `_diag` do runner auto-hospedado sendo utilizado
> `runner-diagnostic-logs` é o nome da pasta que o Github gera quando `ACTIONS_RUNNER_DEBUG` está ativado. Para evitar possíveis confusões, uma pasta com este nome não deve ser criada em outro lugar.
- [ ] Renomeando o diretório `_diag` de um runner auto-hospedado para `runner-diagnostic-logs`
> Renomear o diretório `_diag` nunca deve ser feito, pois isso pode potencialmente afetar as atividades de registro.
