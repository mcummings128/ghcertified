---
question: "Su organización desea reducir el período de retención para los artefactos almacenados, citando preocupaciones de almacenamiento. ¿Cómo se puede hacer esto a nivel organizacional?"
documentation: "https://docs.github.com/en/organizations/managing-organization-settings/configuring-the-retention-period-for-github-actions-artifacts-and-logs-in-your-organization"
---

- [x] Navegando a la configuración de Actions de la organización y editando el valor de la configuración de "Retención de artefactos y registros"
- [ ] Usando self-hosted runners, creando un archivo `.github/retention-policy.yml` y especificando el valor de la clave `artifact-retention-period`
> Personalizar los períodos de retención de artefactos no se limita a self-hosted runners.  
- [ ] Esto no se puede hacer a nivel organizacional. Todos los flujos de trabajo que utilicen `actions/upload-artifact` deben usar el parámetro requerido `retention-days`.
> Aunque el parámetro `retention-days` puede usarse para personalizar el período de retención para artefactos individuales creados por un flujo de trabajo, esto no es apropiado si se intenta aplicar una política general a nivel organizacional. Además, el parámetro `retention-days` es [opcional, no obligatorio](https://github.com/actions/upload-artifact#inputs).
- [ ] Esto no se puede hacer: los artefactos se almacenan estrictamente durante 90 días en todos los sistemas que implementan GitHub Actions. 
> El período de retención predeterminado para los artefactos es de 90 días. Es posible cambiar este valor en todos los sistemas que implementan GitHub Actions. 
