---
question: "¿Qué afirmaciones son ciertas respecto a `github.ref` cuando el flujo de trabajo se activa con un evento `pull_request`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] En solicitudes de extracción que no se han fusionado, `github.ref` se refiere a la referencia completamente formada de la rama/etiqueta de fusión de la solicitud de extracción.  
> Por ejemplo, si el número de la solicitud de extracción (abierta) era #123, `github.ref` sería `refs/pull/123/merge`. Para más información sobre las referencias, consulte la documentación oficial de [Git](https://git-scm.com/book/es/v2/Cap%C3%ADtulo-Interno-Las-Referencias-de-Git).  
- [x] En solicitudes de extracción que han sido fusionadas, `github.ref` se refiere a la referencia completamente formada de la rama a la que se fusionó.  
> Por ejemplo, si estuvieras fusionando algo en la rama `main`, `github.ref` sería `ref/heads/main` después de que se fusionó la solicitud de extracción.  
- [ ] En solicitudes de extracción (independientemente del estado de la fusión), `github.ref` se refiere al número de la solicitud de extracción.  
> Para el evento `pull_request`, el valor de `github.ref` varía dependiendo de si la solicitud de extracción fue fusionada. Este valor siempre será una referencia, no el número de la solicitud de extracción.  
- [ ] En solicitudes de extracción (independientemente del estado de la fusión), `github.ref` es el SHA del último commit de fusión en la rama `GITHUB_REF`.  
> `github.sha` es lo que apunta al último SHA en la rama de fusión (por ejemplo, `refs/pull/PULL_REQUEST_NUMBER/merge`). Consulte la [documentación sobre eventos](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request) para más detalles (buscar `GITHUB_SHA`).  
- [ ] En solicitudes de extracción que no se han fusionado, `github.ref` es la referencia completamente formada del título de la solicitud de extracción.  
> Las referencias no se forman a partir de los títulos de las solicitudes de extracción. `github.event.pull_request.title` es lo que contiene el título de la solicitud de extracción. Consulte la [documentación](https://docs.github.com/en/webhooks/webhook-events-and-payloads#pull_request) para más detalles.  
- [ ] En solicitudes de extracción que han sido fusionadas, `github.ref` es el tipo de referencia completamente formada que activó la ejecución del flujo de trabajo. El valor será `branch`, `tag`, o `null` (si la referencia no estaba completamente formada).  
> `github.ref_type` es el valor del tipo de referencia que activó la ejecución del flujo de trabajo. Solo puede contener `branch` o `tag`; `null` no es un valor válido. Consulte el enlace del documento en esta pregunta para más detalles.  
