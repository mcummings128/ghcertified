---
question: "¿Cómo puedes cambiar el período de retención para los artefactos generados por un determinado workflow?"
documentation: "https://github.com/actions/upload-artifact#inputs"
---

- [x] Utilizando la entrada `retention-days` en `actions/upload-artifact`
- [ ] Utilizando la entrada `retention-days` en `actions/download-artifact`
> `actions/download-artifact` se utiliza para descargar artefactos. Por lo tanto, no influye en cuánto tiempo debe conservarse un artefacto cargado. Además, `retention-days` no es una entrada para esta acción. Consulta [la documentación](https://github.com/actions/download-artifact#inputs) para más detalles.
- [ ] En el repositorio del workflow, navegando a la configuración de Actions y editando el valor de la configuración "Artifact and log retention" para el workflow listado.
> Aunque puedes editar la [configuración "Artifact and log retention"](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-repository) en un repositorio, esta se aplica a todos los workflows dentro de ese repositorio, no a un workflow individual. Esta configuración no enumera workflows individuales.
- [ ] Navegando a la configuración de Actions de la organización y editando el valor de la configuración "Artifact and log retention"
> Aunque puedes editar la [configuración "Artifact and log retention"](https://docs.github.com/en/organizations/managing-organization-settings/configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-organization) en una organización, esta se aplica a todos los workflows dentro de una organización, no a un workflow individual.
