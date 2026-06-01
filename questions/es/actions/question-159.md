---
question: "¿Cuáles de las siguientes afirmaciones son correctas al comparar los eventos pull_request y pull_request_target?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#pull_request"
---

- [x] El evento `pull_request` se ejecuta en el contexto del commit de fusión, mientras que `pull_request_target` se ejecuta en el contexto de la rama predeterminada del repositorio base.
> Para obtener más información sobre los commits de fusión, consulta la [documentación](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges) de GitHub.
- [x] Los flujos de trabajo no se ejecutarán en la actividad de `pull_request` si hay un conflicto de fusión.
- [x] Ambos eventos, `pull_request` y `pull_request_target`, tienen tipos de actividad predeterminados como `opened`, `synchronize` y `reopened`.
- [ ] Se debe tener precaución al usar `pull_request`, ya que las Pull Requests desde forks permitirán que el flujo de trabajo acceda a todos los secrets dentro del repositorio debido a que está asociado con la rama predeterminada.
> Esto es cierto para `pull_request_target`; `pull_request` no está asociado con la rama predeterminada y, por lo tanto, cuando es activado por Pull Requests desde forks, el flujo de trabajo tendrá acceso limitado a los secrets. Consulta la documentación enlazada arriba, específicamente la sección "pull_request_target" para más información.
- [ ] Los flujos de trabajo no se ejecutarán en la actividad de `pull_request_target` si hay un conflicto de fusión.
- [ ] El evento `pull_request_target` debe usarse cuando desees ejecutar el código contenido en los archivos modificados de una Pull Request para realizar cosas como comprobaciones de CI o ejecutar pruebas.
> `pull_request_target` se ejecuta en el contexto de la rama predeterminada del repositorio, lo que puede llevar a que se revise y ejecute código no confiable en actividades como comprobaciones de CI o pruebas. Consulta la [documentación](https://docs.github.com/en/enterprise-cloud@latest/actions/reference/security/secure-use#mitigating-the-risks-of-untrusted-code-checkout) para más información. 
