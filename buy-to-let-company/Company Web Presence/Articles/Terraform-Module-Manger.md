
![[rk-terraform-module-manager.drawio.png]]
This application provides a management view on the state of multiple remote modules, consumers and their environments. Viewers can view data via the RK-Kraken website. It gives a global overview on:

1. All terraform remote modules and the versions available.
2. Consumer versioning
    * Terraform exec version
    * Provider version
    * All remote modules used by consumer and their versions
3. Visualisation of terraform code structure via [Terraform Visual](https://github.com/hieven/terraform-visual)


Data gathered is organised into tables and an alerts section, highlights issues that should be resolved sooner rather than later. This is useful because it allows DevOps to easily spot configuration drift and to ascertain when an infrastructure repository needs updating. Additionally, the creation of rich readme's enable people who are new to a code base get up to speed quickly.

Note that tables in the DynamoDB database are also updated by RK-Terraform-PR-Enforcer after a PR is merged into master.
