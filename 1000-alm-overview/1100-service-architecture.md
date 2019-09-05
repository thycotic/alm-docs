[title]: # (Service Architecture)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (1100)

# Service Architecture

ALM’s service architecture centers on a Windows Service called the Remote Worker.

![ALM Service Architecture](serv-arch.png)

* Running as a suitably privileged Windows Service on your organization’s hardware, the Remote Worker manages interactions among ALM’s cloud service components and aspects of your enterprise infrastructure, such as Active Directory and Secret Server—whether these be on premises, or cloud located like ALM.

The [Getting Started](../5000-get-started/) section provides detailed information on [setting up the Remote Worker](../5000-get-started/5120-setup-remote-wrk/).

![Article End](../../alm-bug.png)

  

  
