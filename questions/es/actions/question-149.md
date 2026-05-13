---
question: "¿Qué hace escribir en `GITHUB_STEP_SUMMARY`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-commands#adding-a-job-summary"
---

```yaml
- name: "Escribir resultados de la suite de pruebas"
  run: |
    echo "Los resultados de la suite de pruebas son:" >> $GITHUB_STEP_SUMMARY
```
- [x] Agrega esta línea al resumen del trabajo
> Escribir en `GITHUB_STEP_SUMMARY` añade al resumen del trabajo, que puede usarse como una versión simplificada de un registro del flujo de trabajo.
- [ ] Agrega esta línea como un subtítulo al nombre del paso en la interfaz de usuario de GitHub Actions
- [ ] Agrega esta línea al artefacto integrado `github-steps-summary.md`
- [ ] Imprime esta línea como un mensaje de depuración a nivel de paso
> Para imprimir un mensaje de depuración en un paso, debes usar la sintaxis `::debug::`. Consulta la sección "Setting a debug message" en la documentación enlazada.
