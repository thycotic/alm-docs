[title]: # (Architecture and Security)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (4500)

# Architecture and Security

ALM’s external architecture relies on a Windows Service called the Remote Worker to manage interactions among ALM’s cloud service components and aspects of your enterprise infrastructure, such as Active Directory and Secret Server, whether on premises or also cloud located.

  
---
  

![ALM External Architecture](arch-02.png)

  
---
  

# Availability

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

## Personally Identifiable Information (PII) and GDPR

ALM requires certain personally identifiable information (PII) to identify each user’s account. This includes the user’s name, email address, and password, these being the minimum necessary for authentication.

ALM tracks IP addresses to support access auditings.

Only select, trusted employees of Thycotic can access customer data and decrypt it, and only by a controlled process that generates an audit trail inaccessible to those employees. This serves the interests of users without compromising their privacy and control.

In GDPR terms, Thycotic customers are the data controllers, and Thycotic is the data processor.

Each ALM customer entirely controls their users, their user roles, and the access to data by their users, according to the policies of the customer organization. ALM logs activity so the customer can monitor access and changes to the secrets, users, and roles, all according to the customer’s policies.

Thycotic conducts a Privacy Impact Assessment (PIA) annually to verify continued conformance to GDPR principles.

## SOC II

Thycotic offers its customers a SOC II Type II Annual Report documenting two rounds of checks. A third party creates the report as an independent assessment of Thycotic’s control environment.

The SOC II report, issued annually in accordance with the AICPA’s AT Section 101 (Attest Engagements) and based on the AICPA’s Trust Services Criteria, addresses the Security, Availability, and Confidentiality criteria.

  
