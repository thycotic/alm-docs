[title]: # (Initial Setup: Outside ALM)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (5300)

## Initial Setup: Outside ALM

Although ALM operates as a cloud service powered by cloud infrastructure, it must interact directly with your organization’s enterprise infrastructure.

* You must install a Windows Service, the ALM Remote Worker, on domain-connected hardware, or directly on a domain controller.

* ALM requires a connection to your organization’s instance of Secret Server.

* To operate within Active Directory on behalf of ALM, the Remote Worker software agent requires an AD account.

This section provides details for each of these setup activities.

