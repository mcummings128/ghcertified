
---
question: "Which of the following are true regarding calling reusable workflows versus calling composite actions?"
documentation: "https://docs.github.com/en/actions/concepts/workflows-and-actions/reusing-workflow-configurations#key-differences-between-reusable-workflows-and-composite-actions"
---

- [x] Composite actions are called via referencing the folder that contains their `action.yml` file.
> As an action, composite actions must contain the brunt of their logic within an `action.yml` file. The composite action's `action.yml` must reside in an `.github/actions/<action-name>` subfolder.
- [ ] Reusable workflows are called via referencing the folder that contains their `action.yml` file.
> Reusable workflows are regular `.yml` or `.yaml` files that are stored in `.github/workflows`. They do not have an `action.yml` file.
- [ ] Composite actions must be called directly from a job.
> Composite actions (as with any other action) are called from within a __step__ of a workflow job--in other words, you do not need a specific workflow job just to caller a composite action. 
- [x] Reusable workflows must be called directly from a job.
> Steps within a workflow job cannot call a reusable workflow. A reusable workflow must be called by an indvidiual job within the caller workflow.  
- [ ] Secrets can be passed to both reusable workflows and calling composite actions via the `uses.secrets` block.
> Only reusable workflows can be called using the `secrets` block. To pass secrets to a composite action, workarounds must be used (such as passing the secret as an input)
- [ ] Only reusable workflows can accept inputs.
> Both reusable workflows and composite inputs can accept inputs. 
- [x] Reusable workflows can use a different runner type than the caller workflow, while composite actions cannot. 
> Reusable workflows have jobs like any other workflow, and those jobs can specify different runner type via the `jobs.runs-on` key. Composite actions inherit the runner environment of their calling workflow job.