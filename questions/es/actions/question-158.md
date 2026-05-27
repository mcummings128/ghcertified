---
question: "Petra está creando un flujo de trabajo cuyo único trabajo se llama `post-merge`. ¿Cómo puede configurar el trabajo para que se active al fusionar una pull request?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#running-your-pull_request-workflow-when-a-pull-request-merges"
---

- [x]  Especificar el tipo de actividad `pull_request` como `closed` y usar una condición a nivel de trabajo para verificar si `github.event.pull_request.merged` es verdadero
```yaml
on:
    pull_request:
        types: [closed]

jobs:
    post-merge:
        if: github.event.pull_request.merged == true
``` 
> Para activar un trabajo de flujo de trabajo cuando se fusiona una pull request, debes especificar tanto el tipo de actividad de la pull request en `on:` como establecer una condición a nivel de trabajo.
- [ ]  Especificar el tipo de actividad `pull_request` como `merged` y usar una condición a nivel de trabajo para verificar si `github.event.pull_request.merged` es verdadero
```yaml
on:
    pull_request:
        types: [merged]
jobs:
    post-merge:
        if: github.event.pull_request.merged == true
``` 
> El evento `pull_request` no tiene un tipo de actividad `merged`. Consulta la sección "pull_request" de la documentación enlazada para ver los tipos de actividad válidos para `pull_request`.
- [ ]  Especificar el tipo de actividad `pull_request` como `merged` (no es necesario una condición a nivel de trabajo)
```yaml
on:
    pull_request:
        types: [merged]
jobs:
    post-merge:
``` 
> El evento `pull_request` no tiene un tipo de actividad `merged`.
- [ ] Especificar el tipo de actividad `pull_request` como `closed` (no es necesario una condición a nivel de trabajo)
```yaml
on:
    pull_request:
        types: [closed]
jobs:
    post-merge:
``` 
> Las pull requests pueden cerrarse sin ser fusionadas. Si no usas una condición correspondiente a nivel de trabajo que verifique si la PR fue fusionada, entonces el trabajo se activará cada vez que se cierre una PR, no solo cuando ocurra una fusión.
- [ ]  Especificar el tipo de actividad `pull_request` como `closed` y usar una condición a nivel de trabajo para verificar si `github.ref` es igual a la rama de fusión de la pull request.
```yaml
on:
    pull_request:
        types: [closed]
jobs:
    post-merge: 
        if: ${{ github.ref == github.event.pull_request.base.ref }}
``` 
> Después de que una pull request ha sido fusionada, `github.ref` será la *referencia completa* de la rama de fusión (ej. `refs/heads/main`), no simplemente la rama de fusión (ej. `main`). 
