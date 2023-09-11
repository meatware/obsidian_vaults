
![[rk_ecr_scanner.drawio.png]]

This app was written to highlight potential security issues with developer written Dockerfiles. It accomplished the following:

1. Switch on 'immutable tags' on misconfigured ECR repos.
2. Switch on 'scan on push' on misconfigured ECR repos.
3. Run a weekly security scan check and publish Critical/High CVE scan results to MS Teams and Confluence.

If this visibility were not provided, it would be likely that app container versions would not be updated and vital security patches would remain unapplied.
