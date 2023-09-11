
![[rk_bamboo_perm_enforcer.drawio.png]]
To facilitate permission management of the on-prem Bamboo server, this python3 app leverages the Bamboo REST API to prevent permission drift and the associated security issues. It does this by:
1. enforcing the use of pre-defined groups such as:
    * developers
    * support
    * design
    * ext-contractors
    * etc
2. Any manually added users and groups were stripped from the permissions unless they were in an exception list. This is definable at the project/plan level.
3. Success/failure sent to MS Teams.