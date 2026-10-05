# Github-Action

## what is git

Git is a distributed version control system that tracks changes in source code during software development.

## what is github action

GitHub Actions is a CI/CD platform that allows you to automate your software development workflows.

## Expression Syntax

use expression to programmatically control `JOBS` and `STEP` based on condition.

**Note** : expression are envoked using `{{ }}`.

**example**

```yaml
# For jab level
jobs:
  deploy:
    if: github.event.workflow_dispatch.inputs.message == 'hello'
    steps:
      - run: echo Hello world ${{ github.actor }}

# For step level
steps:
  - run: echo Hello world ${{ github.actor }}
  - name: skip step
    if: false
    run: echo This step will not run
```

## Contexts

Contexts are objects that provide information about the workflow and the runner.

**Most common contexts**

1. **github**: information about github
2. **env**: information about environment
3. **jobs**: information about jobs
4. **steps**: information about steps
5. **inputs**: information about inputs
6. **secrets**: information about secrets
7. **pull_request**: information about pull request
8. **job**: information about job
9. **vars**: information about variables
10. **runner**: information about runner
11. **strategy**: information about strategy
12. **matrix**: information about matrix

##
