# actions-pr-guidelines
Action that holds the PR Guidelines Workflow

### What does actions-pr-guidelines do for me?



### Working Example

```
name: PR Guidelines Comment

on:
  workflow_call:
  pull_request:
    types:
      - opened
    branches-ignore:
      - 'dependabot/**'
permissions: 
  pull-requests: write
  contents: read

jobs:
  comment:
    runs-on: ubuntu-latest
    steps:
      - uses: hashicorp/actions-pr-guidelines@main
        with:
          token: ${{ secrets.GITHUB_TOKEN }}

```
