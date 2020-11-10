﻿[title]: # (ALM Objects)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (500)

# ALM Objects

ALM relies on four objects to govern Service Accounts: Users, Roles, Groups, and Workflow Templates.

## Users

An ALM **User** object is a proxy for either a **User account** or a **service account** that is **stored in Active Directory**.

* When the ALM User object is a proxy for an Active Directory **User account**, you will perform ALM operations on the ALM proxy purely to control what a person authenticated as that AD User account can do within ALM.

* When the ALM User object is a proxy for an Active Directory **service account**, you will perform ALM operations on the ALM proxy to deliver lifecycle management of the proxied AD service account.

* When you use ALM to create an ALM User object as a proxy for an Active Directory service account that **does not yet exist** in Active Directory, **ALM will create the service account in Active Directory**.

* **After this initial creation** of a service account in Active Directory, ALM operations performed on ALM proxies for AD accounts usually do not directly affect the AD accounts as stored in Active Directory, although there are obvious exceptions such as when an account is disabled.

## Roles

An ALM **Role** defines the privileges that the User has in ALM and the tasks that the User can perform.

* ALM Roles have **nothing to do** with Active Directory Roles and should not be confused with them.

Thycotic provisions ALM with several Roles already set up—Account Owner, Requester, Approver, and System Administrator—and for most organizations these will suffice for initial operations.

### Account Owner

All users automatically have the Account Owner Role. The Account Owner Role is also fixed to the built-in Everyone Group that contains all users in ALM.

This Role provides entry level features and permissions sufficient for a User to read and update managed accounts assigned to them.

### Requestor

Users with the Requestor Role can request the provisioning of new service accounts. Requesters begin each Request by selecting a Workflow Template which determines the lifecycle of the account and the approval process.

### Approver

ALM delivers Requests to Approvers according to the workflow and approval steps specified by the template. An Approver receives notices of account Requests and approves or denies each Request according to the chosen workflow. Some workflows will require multiple Approvers.

On approval, ALM provisions the account and designates the Requestor as the first owner.

### System Administrator

This Role holds all privileges. Organizations use this all-powerful Role to perform initial customer configurations of Account Lifecycle Manager. A System Administrator can provision Users, integrate ALM with external systems, set up ALM Engines, and create Workflow Templates.

Because the System Administrator Role is so highly privileged, its use carries risk of accidental macro-scale changes to your ALM configuration. As a best practice, use the System Administrator Role only for tasks that require its privileges, and when done with those tasks, log out and resume use of less privileged Roles.

### Custom Roles

Once familiar with ALM, you may decide to use the [Custom Roles](custom-roles.md) feature to create Roles that support specific business needs.

* Example: A custom Auditor Role configured with privileges required to view ALM’s Audit Logs but otherwise lacking the full range of privileges given to a System Administrator.

## Groups

An ALM **Group** object defines Groups of ALM User objects that have something in common with each other, such as access to a resource.

* ALM Groups have **nothing to do** with Active Directory Groups and should not be confused with them.

## Workflow Templates

An ALM **Workflow Template** defines a workflow applicable to Requests **made in ALM** for provisioning **in Active Directory** of a service account of a particular type.

* The Workflow Template defines the information that must be provided with the Request, the approval steps that must be completed for the Request to be granted, and who has approval authority at each step.

* Requests for some kinds of service accounts may require just one step, approved by only one person. Requests for other kinds of service accounts may require multiple steps and Approvals by more than one person at some or all of the approval steps.

* Workflow templates also control the selection of BEOL (before end of lifecycle) and AEOL (at end of lifecycle) Notifications ALM sends, when it sends them, and to whom, plus what options the Notifications will offer for managing the service account.
