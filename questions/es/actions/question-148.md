---
question: "¿Cuál afirmación es verdadera respecto a `github.ref` cuando el workflow es activado por un evento de push?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] En eventos de push, `github.ref` es la referencia completamente formada del branch o tag que fue enviado (pushed). 
> Para más información sobre referencias, consulta la [documentación oficial de Git](https://git-scm.com/book/es/v2/Cap%C3%ADtulo-Interno-de-Git-Referencias-en-Git).
- [ ] En eventos de push, `github.ref` es el mensaje del commit que activó el workflow.
> `github.event.head_commit.message` es lo que contiene el mensaje del commit más reciente. Consulta la [documentación](https://docs.github.com/en/webhooks/webhook-events-and-payloads#push) para más detalles.
- [ ] En eventos de push, `github.ref` es el SHA del commit que activó el workflow.
> `github.sha` es lo que apunta al commit SHA. Consulta la [documentación sobre eventos](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows) y el enlace del documento en esta pregunta para más detalles.
- [ ] En eventos de push, `github.ref` es la descripción del commit que activó el workflow.
- [ ] En eventos de push, `github.ref` es el tipo de referencia completamente formada que activó la ejecución del workflow. El valor será `branch`, `tag` o `null` (si la referencia no estaba completamente formada).
> `github.ref_type` es el valor del tipo de referencia que activó la ejecución del workflow. Solo puede contener `branch` o `tag`; `null` no es un valor válido. Consulta el enlace del documento en esta pregunta para más detalles.
