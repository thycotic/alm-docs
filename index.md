[title]: # (ALM Technicals Collection)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (1)

# Introduction to Account Lifecycle Manager

## Overview

### Product

Account Lifecycle Manager (ALM) controls the creation, management, and decommissioning of Active Directory Service Accounts running on your organization's network. ALM reduces Service Account sprawl and increases security by enforcing governance and creating accountability using role-based permissions. Depending on a user's role, they can request, approve, provision, manage, and retire service accounts.

### Key Features

#### Role-Based Access Controls

ALM manages Service Accounts by assigning each account to a User within your organization. ALM uses four **Roles** to define User permissions and determine accountability. A User's Role determines how they interact with ALM and Service Accounts.

* **Account Owner**- All ALM Users are given the Account Owner Role. Account Owners can read and update managed accounts assigned to them.

* **System Administrator**- A System Administrator has full access to ALM's configuration and management. They can create and manage Users, Roles, Groups, and Workflows.

* **Requester**- Requesters can request the provisioning of new service accounts.

* **Approver**- Approvers can approve new service accounts that have been requested.

> Note: ALM roles are distinct from Active Directory Roles. They do not overlap.

#### Workflow Templates

The **System Administrator** can create templates that guide how Service Accounts in your organization are approved and monitored. Templates determine the approval process, review intervals, notification options, and end-of-lifecycle action for Service Accounts.

#### Service Account Discovery Tool

ALM protects your network by controlling newly created privileged accounts. However, you may already have unmanaged Service Accounts running on your network. Using the **Service Account Discovery Tool**, you can scan your network to identify Service Accounts that are active and unmanaged. Using ALM, you can then assign these accounts to Users within your organization or remove the accounts entirely.

### Example Workflow

1. The **System Administrator** installs ALM on your network according to your organization's policies.

    * They create users and assign them Roles.

    * They create a **workflow template** that determines the provisioning process.

2. A User with the **Requester** Role logs into ALM and asks that a Service Account be created.

3. ALM notifies a User with the **Approver** Role that a request has been made.

4. The **Approver** logs into ALM and approves or denies the request.

    * If the request is denied, the **Approver** provides a reason for the denial. ALM notifies the **Requester** of the denial and the reason.

    * If the request is approved, ALM creates a proxy for the requested Service Account within Active Directory. The ALM proxy and the Active Directory account will share the same name. ALM will then notify the **Requester** that the account has been approved and provisioned.

5. Once a service account has been provisioned, ALM monitors the account throughout its lifecycle.
    * The **workflow template** determines the renewal and retirement timeline for the account.
    * ALM will send notifications for upcoming lifecycle events to the selected Users.
    * ALM logs each step for easy auditing.
