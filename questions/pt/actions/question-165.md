---
question: "Como o `repository_dispatch` permite que sistemas externos ao GitHub acionem um workflow?"
documentation: "https://docs.github.com/en/rest/repos/repos?apiVersion=2026-03-10#create-a-repository-dispatch-event"
---

- [x] O sistema externo faz uma requisição POST para a API do GitHub para criar um evento de repository dispatch.
- [x] O workflow é acionado pela criação de um evento de repository dispatch 
> O resultado da ação "Create a repository dispatch event" é um novo evento `repository_dispatch` (webhook), que o `on.repository_dispatch` escuta. 
- [x] A chave de workflow `on.repository_dispatch.types` corresponde ao parâmetro `event_type` no payload da requisição, restringindo o workflow para acionar apenas eventos externos relevantes 
> `on.repository_dispatch.types` permite definir tipos de atividades personalizados. Consulte a [documentação](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#repository_dispatch) para exemplos de como `on.repository_dispatch.types` e `event_type` estão relacionados.
- [ ] O sistema externo faz uma requisição PUT para a API do GitHub para criar um evento de repository dispatch
> O método HTTP correto para a ação "Create a repository dispatch event" é POST.
- [ ] O workflow é acionado por uma requisição POST ao workflow usando o seguinte endpoint `/repos/OWNER/REPO/actions/workflows/<WORKFLOW_ID>/dispatches` 
> Este endpoint corresponde à criação de um evento de workflow dispatch, não um evento de repository dispatch. Além disso, as requisições relacionadas ao Actions devem ser feitas na API do GitHub--não é possível realizar chamadas diretamente ao workflow.
- [ ] A chave de workflow `on.repository_dispatch.event_types` corresponde ao parâmetro `event_type` no payload da requisição, restringindo o workflow para acionar apenas eventos externos relevantes
> Não existe chave `on.repository_dispatch.event_types`. A chave utilizada é `on.repository_dispatch.types`, alinhando-se à forma como outros eventos utilizam `on.<event_name>.types` para filtrar com base na atividade.
