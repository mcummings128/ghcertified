---
question: "¿Cómo se integran los flujos de trabajo con OIDC después de establecer una relación de confianza?"
documentation: "https://docs.github.com/en/actions/concepts/security/openid-connect#how-oidc-integrates-with-github-actions"
---

- [x] Un trabajo del flujo de trabajo solicita un token OIDC del proveedor OIDC de GitHub. El token OIDC es luego validado por el proveedor de nube, que proporciona un token de acceso a la nube para que el flujo de trabajo pueda acceder a los recursos en la nube.
- [ ] Un trabajo del flujo de trabajo solicita un token de acceso a la nube al proveedor de acceso a la nube de GitHub. El token es luego validado por el proveedor de nube, que proporciona un token OIDC para que el flujo de trabajo pueda acceder a los recursos en la nube.
> Primero se solicitan los tokens OIDC, luego se genera un token de acceso a la nube. Los tokens OIDC no pueden acceder a los recursos en la nube.
- [ ] El activador de evento `on: OIDC_request` solicita un token de acceso a la nube al proveedor de acceso a la nube de GitHub. El token es luego validado por el proveedor de nube, lo que permite que el flujo de trabajo acceda a los recursos en la nube.
> No existe un activador de evento `on: OIDC_request`.
- [ ] El activador de evento `on: OIDC_request` solicita un token OIDC al proveedor OIDC de GitHub. El token es luego validado por el proveedor de nube, lo que permite que el flujo de trabajo acceda a los recursos en la nube.
> No existe un activador de evento `on: OIDC_request`.
- [ ] Tras agregar un flujo de trabajo a la lista de "flujos de trabajo permitidos por OIDC" en la configuración del repositorio, los flujos de trabajo crearán automáticamente tokens OIDC y de acceso a la nube por su propia cuenta. Estos tokens luego pueden ser usados inmediatamente en el flujo de trabajo para interactuar con los proveedores de nube.
> No existe una configuración de "flujos de trabajo permitidos por OIDC".  
