---
question: "How many jobs will run in the following matrix?"
documentation: ""
---

```yaml
jobs:
  deploy:
    strategy:
      matrix:
        os: [ubuntu-latest, windows-latest]
        version: [1, 2, 3]
        include:
            - comment-color: "green"
            - error-color: "red"
```

- [x] 6
> When individual keys are added under `include`
- [ ] 8
- [ ]
- [ ]