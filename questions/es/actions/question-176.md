---
question: "Judith tiene un flujo de trabajo que debería activarse cada vez que se realice un commit en el repositorio. El repositorio no siempre está tan activo, por lo que Judith desea que el flujo de trabajo se ejecute programáticamente una vez a la semana como medida de seguridad. ¿Qué combinación de eventos debería usar para imponer este comportamiento?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows"
---

- [x] `push` y `schedule`
- [ ] `pull_request` (con `types:[closed]`) y `schedule`
> Los pull requests pueden cerrarse sin ser fusionados, y se pueden realizar commits en un repositorio sin un pull request.
- [ ] `push` y `workflow_dispatch`
> La palabra "programáticamente" en la pregunta significa que el flujo de trabajo debería activarse de manera no manual. Hacer que los usuarios tengan que activar manualmente un flujo de trabajo cada semana no es confiable; puede y debe automatizarse mediante `schedule`.
- [ ] `push` y `weekly`
> `weekly` no es un evento válido. Usa `schedule` con la sintaxis `cron` para configurar el flujo de trabajo para que se ejecute semanalmente.
- [ ] Esto no es posible: `schedule` no se puede combinar con otros eventos
