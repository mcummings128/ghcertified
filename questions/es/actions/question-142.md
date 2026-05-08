---
question: "¿Cuál de las siguientes respuestas es correcta con respecto a los tokens de acceso de instalación?"
documentation: "https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/authenticating-as-a-github-app-installation#using-an-installation-access-token-to-authenticate-as-an-app-installation"
---

- [x] Los tokens de acceso de instalación son tokens de corta duración ideales para actividades de automatización, pero requieren configurar una GitHub App.
- [x] `GITHUB_TOKEN` es un tipo de token de acceso de instalación.
> `GITHUB_TOKEN` es un token de acceso de instalación de GitHub App que se genera automáticamente para cada ejecución de flujo de trabajo. Consulte la [documentación](https://docs.github.com/en/actions/concepts/security/github_token) para obtener más detalles.
- [x] La acción `actions/create-github-app-token` se puede invocar dentro de los flujos de trabajo para crear un token de acceso de instalación disponible para su uso inmediato.
- [ ] La acción `actions/create-github-app-token` se puede invocar dentro de los flujos de trabajo para crear un token de acceso de instalación, pero el token de acceso de instalación solo se puede usar en futuras ejecuciones del flujo de trabajo. 
> Una vez creado, un token de acceso de instalación puede usarse de inmediato. Consulte la [página oficial para esta acción](https://github.com/actions/create-github-app-token) para obtener más detalles.
- [ ] Los tokens de acceso de instalación no se pueden configurar para actuar en nombre de su GitHub App asociada.
> Los tokens de acceso de instalación a menudo se configuran para actuar en nombre de su GitHub App asociada. Esto puede ayudar en la auditoría de actividades automatizadas.
