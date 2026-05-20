---
question: "You have a workflow job for deploying to an environment. How can the 'UAT' environment be deployed to?"
documentation: "TODO"
---

```yaml

on: pull_request
    types: [closed]
# TODO make a workflow that mods this and uses an env: var with case() based on some workflow input
jobs:
  deploy:
    runs-on: ubuntu-latest
    if: github.event.pull_request.merged
    environment: |-
    ${{ case(
        github.ref == 'refs/heads/environment/main', 'production',
        github.ref == 'refs/heads/environment/preprod', 'preprod',
        startsWith(github.event.pull_request.head.ref, 'feature/uat'), 'UAT',
        'DEV'
    ) }}
```

- [x] By merging a pull request whose source branch begins with `feature/uat`
> `github.event.pull_request.head.ref` refers to a pull request's head branch (also known as a source branch) which contains the changes to be merged.
- [ ] By merging a pull request whose merge branch begins with `feature/uat`
> The merge branch (also known as the target branch) is referenced via `github.event.pull_request.base.ref`
- [ ] By closing a pull request (without merging) whose merge branch is named `feature/uat`
- [ ] By closing a pull request (without merging) whose head branch begins with `feature/uat`
- [ ] UAT cannot be deployed to due to `case()` being set up incorrectly;`environment` will always be set to `DEV`