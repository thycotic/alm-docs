[title]: # (ALM Roles Guide)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (8100)

# ALM Roles Guide

Account Lifecycle Manager’s capabilities are delivered via three primary user roles.

* Requester

* Approver

* System Administrator

You can create additional roles using the Custom Roles feature of ALM.

* An example would be an Auditor role, configured with privileges required to view ALM’s Audit Logs but otherwise lacking the full range of privileges given to a System Administrator.

## ALM Role Definitions

Thycotic provisions ALM to your organization with several roles already set up. For most organizations, these will suffice for initial operations. Once familiar with ALM, you may decide to use the Custom Roles feature to create roles that support specific business needs.

### Requester

People in this role request provisioning of service accounts and lifecycle management for same. Requesters begin each request by selecting a Workflow Template, the specific details of which will drive the rest of request and approval process. The template also controls the specifics of the options selectable for lifecycle management to be applied to the account.

### Approver

ALM delivers requests to Approvers according to the workflow and approval steps specified by the template. An Approver receives notices of account requests and takes steps to approve or deny each request, all in conformance with the given workflow; more than one Approver may need to participate for some accounts.

On approval, ALM provisions the account and designates the Requester as the first owner.

### System Administrator

This role holds all privileges. Organizations use this all-powerful role to perform initial customer configurations of Account Lifecycle Manager. A System Administrator can provision users, integrate ALM with external systems, set up Remote Workers, and create Workflow Templates.

Because the System Administrator role is so highly privileged, its use carries risk of accidental macro-scale changes to your ALM configuration. As a best practice, use the System Administrator role only for tasks that require its privileges, and when done with those tasks, log out and resume use of less privileged roles.

## Custom Roles

ALM System Administrators can create custom roles. To define roles, you review a list of ALM features paired with the permissions potentially applicable to each feature.

* The specific permissions assigned to each role in relation to each ALM feature distinguishes one role from another.

Once you have set the per-feature permissions for a role, you can add users or groups (or both) to the role, thereby granting the role’s privileges to those users, and to users who belong to the groups.

### Functions Applicable to Custom Roles

Functions that pertain to Custom Roles include:

* edit Custom Role name

* enable/disable role

* enable/disable option to have all new users automatically added to the Custom Role

* add/remove users from the Custom Role

* add/remove groups from the Custom Role

## Features

Features are ALM objects to which you can apply privileges in the context of
defining a Custom Role. Features include:

*  **API Token**: All endpoints are controlled by a User’s authentication token set, which is used to obtain a Bearer token for further processing. User access to the API Token feature in the ALM application will allow creation, management, and visibility of API Tokens.

*  **Audit:** Provides a stored log of events that occur within the ALM service. Audit records include user actions within the ALM, ALM system events, as well as remote worker activity.

*  **Configuration:** Ability to define the System Administrator’s email address.

*  **Directory-Service:** Configuration of the Active Directory Service. This includes the External Domain, External Groups, External Users, External Group Mapping, and External OU’s.

*  **Email Notification:** ALM provides a set of stock Email Notification Categories. The Email Notifications are intended to alert various Users and Groups on changes and events relative to their ALM account.

*  **Group:** A Group is a population of Users. Groups can be configured by the customer and manage the Group’s population within ALM. Groups can be assigned to Approval Steps and Account Ownership.

*  **Managed Account:** Service Accounts that are created and managed through ALM.

*  **Provision Approval:** A specific User Role responsible for Reviewing and Approving account Requests made by Requesting Users. A User with Approval rights will be provided access to the Approvals screen in ALM which lists all Requests awaiting an Approver’s Review. The Approver will be able to see all the details of the Request to make their Approval decision.

*  **Provision Template:** Users with the ability to Provision Templates can create Workflow Templates. Workflow Templates are used to define the parameters of the accounts that will be provisioned against the Workflow Template.

*  **Provision Template Workflow:** Permission to Provision Template Workflow feature allows the User to define the Approval Steps required for an account to be Approved that has been Requested against the Workflow Template. Defining Approval Steps involves prescribing Users and/or Groups to Approval Step(s), Steps which are required to be passed for the account to be provisioned for the Request.

*  **Remote Worker:** ALM provides users with the permissions to download the Remote Worker installer. Client-side installed Remote Workers are listed and can assigned to Remote Worker Pools within ALM.

*  **Role:** Roles in ALM allow users with the permissions to assign Users to a specific Role or create Custom Roles. Standard Roles are Requestor, Approver, and System Administrator.

*  **User:** A standard user within ALM will hold one of two Roles, Requestor or Approver, as described above. Users with permissions to the User feature will have the ability to add, remove, or update User accounts.

*  **Vault:** Configuration and management of the Thycotic Secret Server connection to ALM.

*  **Webhook:** Webhooks provide the ability to tie ALM to an external service. ALM provides the ability to Users with permissions to create additional custom webhooks for their business needs.

### Permissions

Permissions confer abilities to take actions within ALM. Distinct permissions within ALM include:

*  **Create**: Ability for role to create a certain features (e.g. Create a managed account)

*  **Read**: Permission to read various features displayed (e.g. Ability to read and have access to the Managed Accounts page of ALM)

*  **Update**: API operation type that allows change to items for their respective feature.

*  **Delete**: Ability to delate items for their respective feature.

*  **Manage**: Acts as a modifier to indicate that the role allows admin access to a respective feature. This will vary from feature to feature on how items can be managed. (e.g. If the role has Manage permissions on the directory-service feature, this would allow the role to perform manual synchronization on Active Directory Objects.)

  


  

