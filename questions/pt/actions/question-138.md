---
question: "Você deseja criar um fluxo de trabalho `Post-Deploy` que realiza atividades relacionadas ao pós-implantação. Qual gatilho de evento o fluxo de trabalho `Post-Deploy` deve usar para que ele seja executado automaticamente após a conclusão de um fluxo de trabalho especificado?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_run"
---

- [x] `workflow_run`
> `workflow_run` permite acionar um fluxo de trabalho assim que outros fluxos de trabalho especificados tiverem sido concluídos (independentemente do sucesso). Note que, embora esta questão pergunte especificamente sobre fluxos de trabalho concluídos, `workflow_run` também pode ser configurado para acionar um fluxo de trabalho quando outros fluxos de trabalho especificados tiverem sido acionados ou iniciado processamento em um runner.
- [ ] `workflow_trigger`
> Não existe tal gatilho de evento.
- [ ] `workflow_dispatch`
> `workflow_dispatch` é usado para acionar manualmente um fluxo de trabalho. Veja [a documentação](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_dispatch) para mais informações.
- [ ] `workflow_call`
> `workflow_call` é usado para que um fluxo de trabalho possa ser chamado a partir de outros fluxos de trabalho ou ações. Veja [a documentação](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_call) para mais informações.
