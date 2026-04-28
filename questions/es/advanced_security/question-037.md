---
question: "¿Qué hace la configuración predeterminada del análisis CodeQL en GitHub?"
documentation: "https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-code-scanning-with-codeql"
---

- [x] Detecta automáticamente los lenguajes, selecciona el conjunto de consultas predeterminado y configura los desencadenantes de análisis
- [ ] Requiere que los usuarios seleccionen lenguajes y definan un conjunto de consultas personalizado antes de que puedan ejecutarse los análisis
> Se muestra un cuadro de diálogo de confirmación al habilitar la configuración predeterminada, pero los lenguajes y el conjunto de consultas se seleccionan automáticamente con antelación
- [ ] Analiza solo el lenguaje principal del repositorio utilizando el conjunto de consultas extendido
> La configuración predeterminada analiza todos los lenguajes compatibles, no solo el principal, y utiliza el conjunto de consultas predeterminado
- [ ] Crea un archivo de flujo de trabajo CodeQL en el repositorio que debe fusionarse antes de que comience el análisis
> Esto describe la configuración avanzada, no la configuración predeterminada
