---
question: "Tienes un flujo de trabajo que utiliza la matriz a continuación. Si un trabajo en la matriz falla, ¿cómo puedes asegurarte de que los demás trabajos en curso y en cola de la matriz no sean cancelados?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#jobsjob_idstrategyfail-fast"
---

```yaml
jobs:
  deploy:
    strategy:
      matrix:
        version: ["1", "1.2", "1.3"]
        os: [ubuntu-latest, windows-latest]
```

- [x] Configurar `jobs.<job_id>.strategy.fail-fast` con `false`
> `jobs.<job_id>.strategy.fail-fast` está configurado como `true` de forma predeterminada, lo que significa que si un trabajo de la matriz falla, los otros trabajos en curso y en cola de la matriz serán cancelados. Debes configurar explícitamente `fail-fast` como `false` para evitar este comportamiento.
- [ ] No se necesita hacer nada, ya que `jobs.<job_id>.strategy.fail-fast` tiene un valor predeterminado de `false`
> `jobs.<job_id>.strategy.fail-fast` está configurado como `true` de forma predeterminada.
- [ ] Configurar `jobs.<job_id>.strategy.matrix.fail-fast` con `false`
> Esto es incorrecto, `fail-fast` está al nivel de `strategy`, no al nivel de `matrix`. Si configuras `fail-fast` al nivel de `matrix`, funcionaría como parte de la [configuración del trabajo](https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/run-job-variations#adding-a-matrix-strategy-to-your-workflow-job) y no afectaría la cancelación/continuación de otros trabajos de la matriz.
- [ ] No se necesita hacer nada, ya que `jobs.<job_id>.strategy.matrix.fail-fast` tiene un valor predeterminado de `false`
> Esto es incorrecto, `fail-fast` está al nivel de `strategy`, no al nivel de `matrix`. 
- [ ] No hay forma de hacer cumplir este comportamiento, no se puede solucionar.
