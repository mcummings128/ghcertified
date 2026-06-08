---
question: "El siguiente workflow llama a un workflow reutilizable en uno de sus trabajos. El workflow reutilizable tiene los `permissions` definidos a nivel de workflow como se ve a continuación. ¿Cuál será el resultado de llamar al workflow reutilizable?"
documentation: "https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows"
---

```yaml
# workflow llamante
on:
    issues:
        types: [opened]
    
    permissions:
        contents: write

    jobs:
        issue_creator:
            permissions:
                contents: read
            uses: ./.github/workflows/issue-creator.yml

# workflow reutilizable (issue-creator.yml)
on:
    workflow_call:

    permissions:
        contents: write

    jobs:
        create_issue:
            runs-on: ubuntu-latest
            steps: 
                env: GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}    
                - run: gh issue create --title "Issue report" --body "Hello!" --repo $GITHUB_REPOSITORY

```
- [x] El workflow reutilizable devolverá un error, ya que el trabajo que lo llamó solo tiene permisos `contents:read`
> En este escenario, el workflow llamante se activa, pero su trabajo no se ejecutará. En su lugar, se generará un error que indica que el archivo del workflow llamante no es válido ya que el workflow reutilizable está solicitando `contents: write`, pero solo tiene permitido `contents: read`.
- [ ] El workflow reutilizable creará un issue en el repositorio titulado `"Issue Report"`
> Esto ocurriría si el trabajo `issue_creator` tuviera permisos `contents:write`, que serían heredados por el workflow reutilizable.
- [ ] El workflow reutilizable no será llamado, ya que los workflows reutilizables deben estar en una subcarpeta de `.github/workflows`
> Todos los workflows deben estar ubicados en el directorio `.github/workflows`.
- [ ] Tanto el workflow llamante como el reutilizable no serán llamados, porque `issues` no es un disparador válido para GitHub Actions. 
> `issues` es un disparador de evento estándar, como se menciona en la [documentación](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#issues).
