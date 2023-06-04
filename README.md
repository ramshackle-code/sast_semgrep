# sast_semgrep
Static Application Security Testing using Semgrep

Reusable Workflow

Call example:

```
name: Static application security testing
on:
  workflow_dispatch:
jobs:
  sast_semgrep:
    permissions:                                                                         
      contents: read
    uses: ramshackle-code/sast_semgrep/.github/workflows/sast_semgrep.yml@[<version-tag> or <commit-sha>]
    secrets:
      token: ${{ secrets.GITHUB_TOKEN }}
```

Optinal parameters

```
     uses: ramshackle-code/sast_semgrep/.github/workflows/sast_semgrep.yml@[<version-tag> or <commit-sha>]
     with:
       timeout-minutes: <minutes>     #Execution timeout. Default value 5 minutes
       semgrep-version: <image tag>   #Image tag. Default value 1.24
       runs-on: <runner label>        #Runner Label. Default 'ubuntu-latest'
```
