# 🚀 ThomasvZadelhoff - Continuous integration

This repository serves as a `GitOps` repo.

## Using the workflows

### For PHP applications (`symfony` & `laravel`)
```yaml
jobs:
  ci-php:
    uses: ThomasvZadelhoff/continuous-integration/.github/workflows/php.yml@main
    with:
      project: argocd_project_name
      application: argocd_application_name
      application_type: symfony
      build_worker: false
    secrets:
      token: ${{ secrets.PAT }}
```

### For Next.js applications
```yaml
jobs:
  ci-next-js:
    uses: ThomasvZadelhoff/continuous-integration/.github/workflows/next-js.yml@main
    with:
      project: argocd_project_name
      application: argocd_application_name
    secrets:
      token: ${{ secrets.PAT }}
```

---
*Crafted by [Thomas van Zadelhoff](https://thomasvanzadelhoff.nl) under the [MIT](https://choosealicense.com/licenses/mit/) license.*