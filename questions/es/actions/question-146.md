---
question: "¿Qué declaraciones son verdaderas respecto a `github.ref` cuando el workflow es activado por un evento `pull_request`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] En solicitudes de extracción que no han sido fusionadas, `github.ref` se refiere a la referencia completamente formada de la rama/etiqueta de fusión del pull request. 
> Para más información sobre referencias, consulta la [documentación oficial de Git](https://git-scm.com/book/en/Git-Internals-Git-References).
- [x] En solicitudes de extracción que han sido fusionadas, `github.ref` se refiere a la referencia completamente formada de la rama en la que se realizó la fusión.
- [ ] En solicitudes de extracción (independientemente del estado de fusión), `github.ref` se refiere al número del pull request. 
> Para el evento `pull_request`, el valor de `github.ref` varía dependiendo de si la solicitud de extracción fue fusionada. Este valor siempre será una referencia, no el número del pull request.
- [ ] En solicitudes de extracción (independientemente del estado de fusión), `github.ref` es el SHA del último commit de fusión en la rama `GITHUB_REF`.
> `github.sha` es lo que apunta al último SHA en la rama de fusión (por ejemplo, `refs/pull/PULL_REQUEST_NUMBER/merge`). Consulta la [documentación de eventos](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request) para más detalles (busca `GITHUB_SHA`).
- [ ] En solicitudes de extracción que no han sido fusionadas, `github.ref` es la referencia completamente formada del título del pull request. 
> Las referencias no se forman a partir de los títulos de los pull requests. `github.event.pull_request.title` es lo que contiene el título del pull request. Consulta la [documentación](https://docs.github.com/en/webhooks/webhook-events-and-payloads#pull_request) para más detalles.
- [ ] En solicitudes de extracción que han sido fusionadas, `github.ref` es el tipo de referencia completamente formada que activó la ejecución del workflow. El valor será `branch`, `tag` o `null` (si la referencia no estaba completamente formada).
> `github.ref_type` es el valor del tipo de referencia que activó la ejecución del workflow. Solo puede contener `branch` o `tag`; `null` no es un valor válido. Consulta el enlace del documento en esta pregunta para más detalles.
