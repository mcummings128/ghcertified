---
question: "¿Cómo ejecutas scripts personalizados de JavaScript directamente en un flujo de trabajo de GitHub Actions?"
documentation: "https://github.com/marketplace/actions/github-script"
---

- [x] A través de la acción `actions/github-script`
> `actions/github-script` te permite escribir y utilizar JavaScript en línea para realizar llamadas a la API y acceder al contexto del flujo de trabajo. Para usar `actions/github-script`, se llama de la misma manera que a cualquier otra acción, como se muestra en la [documentación](https://github.com/actions/github-script). 
- [ ] Habilitando la configuración 'Permitir scripts personalizados de JavaScript' en los ajustes de Actions de un repositorio
> No existe una configuración 'Permitir scripts personalizados de JavaScript' en los ajustes de Actions de un repositorio.
- [ ] Habilitando la configuración 'Permitir scripts personalizados de JavaScript' en los ajustes de Actions de una organización
> No existe una configuración 'Permitir scripts personalizados de JavaScript' en los ajustes de Actions de un repositorio. Aunque es posible que debas habilitar configuraciones como 'Permitir acciones creadas por GitHub' en los ajustes de Actions de una organización para usar acciones oficiales de GitHub, esto no está relacionado únicamente con `actions/github-script`. 
- [ ] Escribiendo el contenido de un bloque de script en la variable ambiental `GITHUB_SCRIPT`
> `GITHUB_SCRIPT` no es una variable ambiental predeterminada de GitHub Actions. Una lista de variables ambientales predeterminadas se puede encontrar en la [documentación](https://docs.github.com/en/actions/reference/workflows-and-actions/variables).
- [ ] En una acción de JavaScript, configurando la clave `using` a `'github-script'`
> Las acciones de JavaScript deben tener la clave `using` configurada en `node*`, donde * es una versión compatible de Node.js. Generalmente, las acciones de JavaScript no necesitan `actions/github-script`.
