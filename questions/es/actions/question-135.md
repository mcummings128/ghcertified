---
question: "Has bifurcado un repositorio para mejorar un flujo de trabajo que utiliza un secreto para acceder a una aplicación de terceros. Ejecutas el flujo de trabajo antes de editar su código para obtener un resultado de referencia, pero descubres que el flujo de trabajo falla. ¿Por qué ocurriría esto?"
documentation: "https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/use-secrets?tool=webui#using-secrets-in-a-workflow"
---

- [x] Los repositorios bifurcados no heredan los secretos del repositorio original  
> Como medida de seguridad, (excepto por el `GITHUB_TOKEN`) los secretos no se pasan al runner cuando un flujo de trabajo se ejecuta desde un repositorio bifurcado. Esto provocará que el flujo de trabajo falle si hace referencia a un secreto del repositorio original.
- [ ] Al heredar el secreto del repositorio original, ocurrió un error durante la bifurcación que resultó en un secreto mal formado o inválido  
> Excepto por el `GITHUB_TOKEN`, los secretos no se pasan al runner cuando un flujo de trabajo se ejecuta desde un repositorio bifurcado. Por lo tanto, no podría ocurrir tal malformación.
- [ ] El secreto heredado tenía un tamaño mayor a 48 KB  
> Excepto por el `GITHUB_TOKEN`, los secretos no se pasan al runner cuando un flujo de trabajo se ejecuta desde un repositorio bifurcado. Por lo tanto, el tamaño no es un factor a considerar.
- [ ] Los repositorios bifurcados solo heredan los secretos del repositorio, por lo que el secreto utilizado en el flujo de trabajo debe haber sido un secreto organizacional o de entorno.  
> Excepto por el `GITHUB_TOKEN`, los secretos no se pasan al runner cuando un flujo de trabajo se ejecuta desde un repositorio bifurcado. Esto aplica a todos los tipos de secretos (repositorio, entorno y organizacional).
