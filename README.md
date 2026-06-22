# FinsOpsIQ Workflow Catalog

This repository stores reference copies of the CI/CD workflows used by the FinsOpsIQ repositories.

The runnable workflows remain in their owning repositories:

| Area | Owning repository | Runnable workflow path |
| --- | --- | --- |
| Application PR validation | `AzureFinOpsIQ/FinOpsIQ-App` | `.github/workflows/build.yml` |
| Application release build | `AzureFinOpsIQ/FinOpsIQ-App` | `.github/workflows/release.yml` |
| Helm / AKS deployment | `AzureFinOpsIQ/FinOpsIQ-Helm` | `.github/workflows/aks-deploy.yml` |
| Terraform infrastructure | `AzureFinOpsIQ/FinOpsIQ-Infra` | `.github/workflows/terraform-infra.yml` |
| Terraform backend bootstrap | `AzureFinOpsIQ/FinOpsIQ-Infra` | `.github/workflows/bootstrap-backend.yml` |

## Catalog Layout

```text
app/
  build.yml
  release.yml

helm/
  aks-deploy.yml

infra/
  bootstrap-backend.yml
  terraform-infra.yml
```

## Important

These files are catalog/reference copies. GitHub Actions executes workflows from each product repository's `.github/workflows/` directory.

When a workflow changes in an owning repository, update the corresponding catalog copy here to keep the delivery model documented.
