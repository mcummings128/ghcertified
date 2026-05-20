---
question: "Marianne tiene una rama de funcionalidad que contiene su nuevo archivo de workflow, el cual está configurado para activarse a las 2 AM todos los días, utilizando la sintaxis que se muestra a continuación. Sin embargo, al día siguiente, el workflow no se activa. ¿Cuál podría ser la razón?"
documentation: "https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule"
---

```yaml
on:
    schedule:
        cron:
            "0 2 * * *"
```

- [x] El archivo de workflow debe existir en la rama predeterminada para ser activado por el evento `schedule`
- [ ] La sintaxis de `cron` no está programada correctamente
> `"0 2 * * *"` en la sintaxis CRON significa "ejecutarse todos los días a las 2 AM." Incluso si la programación estuviera incorrecta, el workflow aún no se activaría, ya que no está presente en la rama predeterminada.
- [ ] `schedule` no puede ser el único evento en el workflow. Debe estar acompañado de un evento basado en el repositorio, como `push`
- [ ] No se utilizó la sintaxis `@daily`
> La sintaxis CRON no estándar como `@daily` no es compatible con GitHub Actions.
- [ ] El repositorio privado que contiene el workflow no ha tenido ninguna actividad en más de 60 días, lo que desactiva automáticamente el workflow.
> Esta desactivación automática solo ocurre en los repositorios públicos, no en los privados.
