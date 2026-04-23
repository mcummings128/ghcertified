<!-- TODO CHANGE QUESTION NUMBER BASED ON OFFICIAL GH RESPONSE-->
---
question: "What keys are required to create a composite action?"
documentation: "TODO"
---

- [x] `name`,`runs.using: composite`,`runs.steps`
- [ ] `name`,`description`,`runs.using: composite`,`runs.steps`
> The `description` key is not strictly required, but it is highly recommended. 
- [ ] `name`,`runs-on: composite`,`runs.steps`
> The `runs-on` key is for workflows, not composite actions. 
- [ ] `name`,`runs.using: composite-action`,`runs.jobs`
> `runs.jobs` is not a valid key for actions of any type.
