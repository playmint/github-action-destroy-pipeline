# github-action-destroy-pipeline

deletes a concourse pipeline from a github action

## Example

Destroy a concourse pipeline:

```yaml
on:
  push:
    branches:
    - main

jobs:
  test:
    runs-on: ubuntu-latest
    name: Destroy a concourse pipeline
    steps:

    - name: destroy_pipeline
      uses: playmint/github-action-destroy-pipeline@v1
      with:
        url: ${{ secrets.CONCOURSE_URL }}
        username: ${{ secrets.CONCOURSE_USERNAME }}
        password: ${{ secrets.CONCOURSE_PASSWORD }}
        team: main
        pipeline-name: action-example
```


