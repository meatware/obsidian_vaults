
![[release_page_generator.drawio.png]]

The company releases multiple new software versions from different Dev teams every Saturday. This app generates a rich release page table in confluence by making API calls to JIRA, Bamboo and Confluence. Whilst this is an ostensibly simple application, it possesses additional features that made it indispensable for all the teams that help with the release process. i.e. Developers, DevOps, Support, QA and Management.

1. The app auto-updates the release table every 30 minutes, but preserves manually made Confluence edits in certain columns such as:
    * QA Testing & Deploy notes - preserves text and rich media elements such as embedded pictures.
    * CCB Production Change tickets: place for JIRA ticket that details what the change is. After the change is completed, the Confluence preview of the ticket is struck-through to indicate completion.
    * Attached database sql files, etc.
2. Showed number of Dev tickets left to complete in release (6/12). (So we know if the release will make it prior to Thurs 1300 CCB release cut-off)
3. Displays the app version currently deployed to UAT and PROD. If the planned release version has not been released into UAT, by the Thurs 1300 cut-off, the release date will have to be postponed.
4. Displays release notes generated from Jira release version description
5. Remembers and fills in which group is responsible for deploying the app. Usually Support or DevOps.
6. Failures logged to MS Teams