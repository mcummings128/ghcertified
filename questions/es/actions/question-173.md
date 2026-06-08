---
question: "Una organización tiene varios repositorios que comparten un entorno especializado de Node.js alojado en una red privada. El próximo objetivo de la organización involucra la configuración de un software de bloqueo de nodos dentro de esa red. ¿Cuál de las siguientes opciones se adapta mejor a las necesidades de la organización cuando se trata de ejecutar workflows?"
documentation: "https://docs.github.com/en/actions/concepts/runners/self-hosted-runners"
---

- [x] Runners auto-hospedados configurados a nivel de organización
- [ ] Un runner auto-hospedado por repositorio, configurado a nivel de repositorio
> Esto sería redundante y complejo de gestionar. Los repositorios pueden referenciar el mismo runner a nivel de organización, lo cual es el enfoque correcto en esta situación.
- [ ] Runners hospedados por GitHub, con todos los workflows utilizando `actions/setup-node`
> Los runners hospedados por GitHub son [efímeros](https://docs.github.com/en/actions/concepts/runners/github-hosted-runners#overview-of-github-hosted-runners), lo que significa que se configura una nueva instancia del runner para cada ejecución del workflow. Esto no funcionaría bien con el software de bloqueo de nodos, que solo permite que el software se ejecute en un dispositivo/VM especificado. Además, aunque los runners hospedados por GitHub pueden configurarse para acceder a redes privadas, esta no es una funcionalidad que venga preconfigurada.
- [ ] Runners hospedados por GitHub configurados a nivel de organización
> Los runners hospedados por GitHub no pueden configurarse de esta manera.
- [ ] Runners hospedados por GitHub, utilizando `runs-on: [node<version>]` (`<version>` siendo la versión deseada de Node) en todos los workflows.
> `[node<version>]` no hace referencia a ningún runner hospedado por GitHub.
