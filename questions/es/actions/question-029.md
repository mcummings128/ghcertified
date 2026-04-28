---
question: "Tu flujo de trabajo de análisis de Pull Request utiliza múltiples herramientas de análisis de código y tarda unos 20 minutos en completarse por completo. Se activa en el evento `pull_request` con el filtro `branches` configurado como `master`. Por lo tanto, si un desarrollador envía varios commits en pocos minutos, múltiples flujos de trabajo se ejecutan en paralelo. ¿Cómo puedes detener todas las ejecuciones de flujo de trabajo anteriores y ejecutar solo la que contiene los cambios más recientes?"
documentation: "https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#example-using-concurrency-to-cancel-any-in-progress-job-or-run"
---

- [x] Usa concurrencia con cancel-in-progress
```yaml
concurrency:
  group: ${{ github.workflow }}-${{ github.ref }}
  cancel-in-progress: true
```
- [ ] Usa concurrencia
```yaml
concurrency:
  group: ${{ github.ref }}
```
> Esto pondría en cola las ejecuciones en esa referencia de GitHub. No detendrá las ejecuciones anteriores.

- [ ] Usa el filtro de tipos de actividad
```yaml
on:
  pull_request:
    branches:
      - master
    types: [latest]
```
> No existe un tipo de actividad como `latest` para el evento pull_request.

- [ ] Usa la bandera cancel-in-progress para el evento `pull_request`
```yaml
on:
  pull_request:
    branches:
      - master
    cancel-in-progress: true
```
> `cancel-in-progress` solo se puede usar dentro de un bloque de `concurrency`. No es una clave válida para `pull_request`.
