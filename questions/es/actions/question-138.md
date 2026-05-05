---
question: "Quieres crear un flujo de trabajo `Post-Deploy` que realice actividades relacionadas con la post-implementación. ¿Qué evento disparador debería usar el flujo de trabajo `Post-Deploy` para que se ejecute automáticamente después de que se complete un flujo de trabajo especificado?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_run"
---

- [x] `workflow_run`
> `workflow_run` te permite disparar un flujo de trabajo una vez que otros flujos de trabajo especificados se han completado (independientemente de si tuvieron éxito). Ten en cuenta que, aunque esta pregunta se refiere específicamente a flujos de trabajo completados, `workflow_run` también puede configurarse para disparar un flujo de trabajo cuando otros flujos de trabajo especificados han sido iniciados o están siendo procesados en un runner.
- [ ] `workflow_trigger`
> No existe tal evento disparador.
- [ ] `workflow_dispatch`
> `workflow_dispatch` se utiliza para disparar un flujo de trabajo manualmente. Consulta [la documentación](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_dispatch) para más información.
- [ ] `workflow_call`
> `workflow_call` se utiliza para que un flujo de trabajo pueda ser llamado desde otros flujos de trabajo o acciones. Consulta [la documentación](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#workflow_call) para más información.
