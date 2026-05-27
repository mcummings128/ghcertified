---
question: "¿Por qué deberías usar OIDC al conectar un workflow con proveedores de la nube?"
documentation: "https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/about-security-hardening-with-openid-connect"
---

- [x] OIDC evita que tengas que mantener credenciales de la nube como secretos de GitHub de larga duración 
- [x] OIDC implica la generación y uso de tokens de corta duración, lo cual es más seguro
- [ ] Los proveedores de la nube requieren el uso de OIDC.
> OIDC es opcional y recomendado, pero no estrictamente necesario.
- [ ] Usar OIDC te permite eludir la configuración de políticas de confianza con los proveedores de la nube
> Debes configurar políticas de confianza con el proveedor de la nube para poder usar OIDC
- [ ] OIDC genera tokens web JSON (JWTs) que pueden ser utilizados en trabajos de workflow
> La infraestructura de OIDC implica crear JWTs que son únicos para cada trabajo de workflow
- [ ] Usar OIDC dentro de un workflow guardará automáticamente los registros de ese workflow en el almacenamiento en la nube
> OIDC se ocupa de la seguridad al conectarse a proveedores de la nube, no del almacenamiento. Por lo tanto, no está involucrado en guardar registros de los workflows en ningún lugar.
