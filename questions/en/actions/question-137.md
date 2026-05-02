---
question: "How many jobs will run in the following matrix?"
documentation: ""
---

```yaml
jobs:
  deploy:
    strategy:
      matrix:
        version: ["1", "1.2", "1.3"]
        os: [ubuntu-latest, windows-latest]
```