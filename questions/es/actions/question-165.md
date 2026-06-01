---
question: "¿Cómo permite `repository_dispatch` que sistemas externos a GitHub desencadenen un workflow?"
documentation: "https://docs.github.com/en/rest/repos/repos?apiVersion=2026-03-10#create-a-repository-dispatch-event"
---

- [x] El sistema externo realiza una solicitud POST a la API de GitHub para crear un evento de repository dispatch.
- [x] El workflow se activa con la creación de un evento de repository dispatch
> El resultado del "Crear un evento de repository dispatch" es un nuevo evento `repository_dispatch` (webhook), que es escuchado por `on.repository_dispatch`. 
- [x] La clave `on.repository_dispatch.types` del workflow corresponde al parámetro `event_type` en el payload de la solicitud, restringiendo que el workflow solo se activen en eventos externos relevantes 
> `on.repository_dispatch.types` te permite definir tipos de actividad personalizada. Consulta la [documentación](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#repository_dispatch) para ejemplos de cómo `on.repository_dispatch.types` y `event_type` se relacionan entre sí.
- [ ] El sistema externo realiza una solicitud PUT a la API de GitHub para crear un evento de repository dispatch
> El método HTTP correcto para "Crear un evento de repository dispatch" es POST.
- [ ] El workflow se activa mediante una solicitud POST al workflow utilizando el siguiente endpoint `/repos/OWNER/REPO/actions/workflows/<WORKFLOW_ID>/dispatches`
> Este endpoint corresponde a crear un evento de workflow dispatch, no un evento de repository dispatch. Además, la API de GitHub es donde deberían realizarse las solicitudes relacionadas con Actions; no se pueden realizar llamadas API directamente al workflow.
- [ ] La clave `on.repository_dispatch.event_types` del workflow corresponde al parámetro `event_type` en el payload de la solicitud, restringiendo que el workflow solo se active en eventos externos relevantes
> No existe una clave `on.repository_dispatch.event_types`. Se utiliza `on.repository_dispatch.types`, en línea con cómo otros eventos usan `on.<event_name>.types` para filtrar según la actividad.
