---
question: "Las acciones de JavaScript y `actions/github-script` usan JavaScript. ¿Por qué deberías usar `actions/github-script` en lugar de crear tu propia acción de JavaScript?"
documentation: "https://github.com/actions/github-script"
---

- [x] `actions/github-script` debería usarse para scripts cortos en línea
- [x] `actions/github-script` debería usarse cuando quieras usar un cliente preautenticado para interactuar con la API de GitHub.
- [x] Las acciones de JavaScript deberían usarse cuando quieras una acción personalizada reutilizable que pueda utilizarse en varios repositorios
- [ ] Las acciones de JavaScript deberían usarse para scripts cortos en línea
- [ ] `actions/github-script` debería usarse cuando necesites utilizar un entorno de Node.js ajustado con varias dependencias específicas
> Aunque puedes instalar módulos para que los use `actions/github-script` antes de llamarlo, si se requieren varias dependencias, esto resulta en varios pasos en el flujo de trabajo. Además, `actions/github-script` no te permite cambiar la versión de Node.js; estás limitado a la que define.
- [ ] Las acciones de JavaScript deberían usarse cuando quieras una solución de bajo costo para realizar llamadas a la API de GitHub.
> Las acciones de JavaScript no tienen bajo costo; requieren crear un archivo `action.yml`, el cual a su vez debe almacenarse en su propia carpeta o incluso en su propio repositorio, dependiendo del enfoque. `actions/github-script` viene con un cliente preautenticado que facilita las llamadas a la API de GitHub utilizando un enfoque basado en JavaScript.
