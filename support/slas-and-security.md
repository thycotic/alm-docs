[title]: # (SLAs and Related Operational Considerations)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (8520)

# SLAs and Related Operational Considerations

Account Lifecycle Manager offers a 99.9% Uptime SLA based on the Azure uptime SLAs of its component products and services.

## Business Continuity

Every 5 to 10 minutes, ALM backs up transaction logs to local storage. This supports a Recovery Point Objective (RPO) of ten minutes.

Every hour, ALM backs up transaction logs to a geographically redundant location, supporting an RPO of 1 hour.

ALM also creates differential backups approximately every 12 hours, and full database backups approximately every 24 hours.

## Disaster Recovery

The failure of an entire Azure Region would cause complete loss of access to Thycotic’s cloud entities located in the failed region for an indefinite, ongoing time.

To recover from such, Thycotic would rebuild an ALM instance in another Azure region. The target for rebuilding and connecting to the geographically redundant database is 12 hours, although Thycotic cannot guarantee that target.

## Confidentiality

### Data-at-rest

ALM encrypts some critical data, including requests, audits, Secret Server connection information, and any other stored credentials such as API Tokens.

Encryption transparently applies to all data stored in the Azure SQL Server databases. This includes application audit logging. ALM does not encrypt the Remote Worker logs.

### Data-in-Transit

ALM establishes HTTPS connections in conformance with TLS 1.2 protocols. This includes API and Remote Worker connections.

## Client Authentication

Authentication proceeds using OIDC to Thycotic One.

## Integrity: Code Signing

Code signing applies to the Remote Worker software, which is downloaded to the customer’s premises to coordinate interactions among ALM and the customer’s Active Directory and Secret Server resources.



  

  
