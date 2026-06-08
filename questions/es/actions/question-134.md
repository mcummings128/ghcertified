---
question: "¿Cómo se ejecutan scripts personalizados de JavaScript directamente en un flujo de trabajo de GitHub Actions?"
documentation: "https://github.com/marketplace/actions/github-script"
---

- [x] A través de la acción `actions/github-script`
> `actions/github-script` te permite escribir y utilizar JavaScript en línea para realizar llamadas a la API y acceder al contexto del flujo de trabajo. Para usar `actions/github-script`, se llama como cualquier otra acción, como se muestra en la [documentación](https://github.com/actions/github-script) 
- [ ] Habilitando la configuración 'Allow custom JavaScript scripts' en los ajustes de Actions de un repositorio
> No existe una configuración llamada 'Allow custom JavaScript scripts' en los ajustes de Actions de un repositorio.
- [ ] Habilitando la configuración 'Allow custom JavaScript scripts' en los ajustes de Actions de una organización
> No existe una configuración llamada 'Allow custom JavaScript scripts' en los ajustes de Actions de un repositorio. Aunque puede que debas habilitar configuraciones como 'Allow actions created by Github' en los ajustes de Actions de una organización para usar acciones oficiales de GitHub, esto no está relacionado específicamente con `actions/github-script`. 
- [ ] Escribiendo el contenido de un bloque de script en la variable de entorno `GITHUB_SCRIPT`
> `GITHUB_SCRIPT` no es una variable de entorno predeterminada de GitHub Actions. Una lista de variables de entorno predeterminadas se puede encontrar en la [documentación](https://docs.github.com/en/actions/reference/workflows-and-actions/variables)
- [ ] En una Acción de JavaScript, estableciendo la clave `using` en `'github-script'`
> Las Acciones de JavaScript deben tener la clave `using` configurada en `node*`, donde `*` es una versión compatible de Node.js. Generalmente, las Acciones de JavaScript no necesitan `actions/github-script`.
