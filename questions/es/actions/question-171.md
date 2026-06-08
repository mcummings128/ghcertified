---
question: "¿Por qué volverías a ejecutar un flujo de trabajo en lugar de generar una nueva ejecución?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-workflow-runs/re-run-workflows-and-jobs"
---

- [x] Volver a ejecutar un flujo de trabajo te permite volver a ejecutar trabajos de flujo de trabajo que fallaron, en lugar de generar una nueva ejecución que ejecutará todos los trabajos.
- [x] Volver a ejecutar un flujo de trabajo significa que los trabajos del flujo de trabajo se ejecutan en el mismo contexto del commit SHA y la referencia git del evento original que activó el trabajo.
- [x] Volver a ejecutar un flujo de trabajo te permite habilitar un registro de depuración adicional para los trabajos seleccionados.
- [ ] Volver a ejecutar un flujo de trabajo asegura que `GITHUB_TRIGGERING_ACTOR` permanezca sin cambios, por lo que no hay ambigüedad sobre quién activó originalmente el flujo de trabajo.
> Según la [documentación](https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context), el valor de `GITHUB_TRIGGERING_ACTOR` se actualiza según quién volvió a ejecutar el flujo de trabajo.  
- [ ] Volver a ejecutar un flujo de trabajo asegura que `GITHUB_ACTOR` se actualice, por lo que no hay ambigüedad sobre quién volvió a ejecutar el flujo de trabajo.
> Según la [documentación](https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context), el valor de `GITHUB_ACTOR` es quien activó originalmente el flujo de trabajo; no cambia al volver a ejecutar un flujo de trabajo.
- [ ] Volver a ejecutar un flujo de trabajo sobrescribe las ejecuciones de trabajos fallidos, haciendo que las ejecuciones parezcan más directas.
> Las ejecuciones de trabajos fallidos permanecen cuando se vuelve a ejecutar un trabajo. Usando la interfaz de usuario, es fácil alternar entre la ejecución original del trabajo y las re-ejecuciones posteriores.  
