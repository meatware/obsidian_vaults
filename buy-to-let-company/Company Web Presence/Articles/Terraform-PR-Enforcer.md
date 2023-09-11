
![[rk_terraform_pr_enforcer.drawio.png]]
Tests PR merges for errors:
1. Checks all code entry points in repo (not just the modified state files) by running terraform init, validate and plan.
2. Enforces minimum provider version. e.g. AWS provider must be > 4.0.0
3. Enforces minimum terraform exe version. e.g. terraform binary must be > 1.0.0
4. Checks all variables have types and types.
5. Runs terraform fmt
6. Ensures README.md files are created using terraform-docs
7. Ensure consumers are using s3 backed remote state
8. Ensures remote modules, terraform exe and aws providers are pinned to the correct semantic version.
9. Can be easily extended to run other static analysis tools such as tflint, checkov 2.0, etc