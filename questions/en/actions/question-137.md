---
question: "How many jobs will run in the following matrix?"
documentation: "https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/run-job-variations#expanding-or-adding-matrix-configurations"
---

```yaml
jobs:
  test_deploy:
    strategy:
      matrix:
        os: [ubuntu-latest, windows-latest]
        version: [1, 2]
        include:
            - comment-color: "green"
            - error-color: "red"
            - os: "ubuntu-latest"
              comment-color: "blue"
            - os: "macos-latest"
              comment-color: "yellow"
```

- [x] 5
> This matrix produces 5 jobs with the following matrix combinations:
> **os:ubuntu-latest,version:1,comment-color:blue,error-color:red**
> **os:ubuntu-latest,version:2,comment-color:blue,error-color:red**
> **os:windows-latest,version:1,comment-color:green,error-color:red**
> **os:windows-latest,version:2,comment-color:green,error-color:red**
> **os:macos-latest,comment-color:yellow**

> For jobs that use `os:ubuntu-latest`, the `comment-color` will be `"blue"` because `comment-color` is not part of the original matrix configuration, so it can be overwritten by other mentions of itself. 

> All jobs originating from combinations of the original will use `error-color:red` because `error-color` does not overwrite any combinations in the original matrix, and will thus get added to each said configuration. It is only defined once, meaning it will always be `"red"` 

> The last job is made from the last set of configurations in `include`. `{os:macos-latest,comment-color:yellow}` cannot be added to any original matrix combination without overwriting a value (in this case, `os`), so a new job must be made. This job will not have `error-color` in it because `error-color` is not part of the original matrix configuration. While `comment-color` is also not in the original matrix configuration, it __is__ included as part of the last set of configurations.  
- [ ] 6
- [ ] 7
- [ ] 10