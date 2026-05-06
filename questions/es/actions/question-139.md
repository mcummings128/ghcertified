---
question: "¿De qué maneras puedes habilitar el registro de diagnóstico del runner?"
documentation: "https://docs.github.com/en/actions/how-tos/monitor-workflows/enable-debug-logging#enabling-runner-diagnostic-logging"
---

- [x] Configurando un secreto o una variable llamada `ACTIONS_RUNNER_DEBUG` como `true`
> Nota: `ACTIONS_RUNNER_DEBUG` se puede configurar como un secreto o una variable a nivel de organización o a nivel de repositorio.
- [x] Volviendo a ejecutar un workflow con `Enable debug logging enabled`
- [ ] Agregando una carpeta de nivel superior llamada `ACTIONS_RUNNER_DEBUG` al repositorio del workflow
- [ ] Agregando una subcarpeta llamada `runner-diagnostic-logs` al directorio `_diag` del runner auto-hospedado que se está utilizando
> `runner-diagnostic-logs` es el nombre de la carpeta que GitHub genera cuando se habilita `ACTIONS_RUNNER_DEBUG`. Para evitar posibles confusiones, no se debe crear una carpeta con este nombre en ningún otro lugar.
- [ ] Renombrando el directorio `_diag` de un runner auto-hospedado a `runner-diagnostic-logs`
> Nunca se debe renombrar el directorio `_diag`, ya que esto podría afectar potencialmente las actividades de registro.
