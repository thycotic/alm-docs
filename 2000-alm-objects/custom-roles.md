[title]: # (Custom Roles)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (2100)

# Custom Roles

ALM System Administrators can create Custom Roles. To define Roles, you review a list of ALM features paired with the permissions potentially applicable to each feature.

* The specific permissions assigned to each Role in relation to each ALM feature distinguishes one Custom Role from another.

Once you have set the per-feature permissions for a Role, you can add Users or Groups (or both) to the Role, thereby granting the Role’s privileges to those Users, and to Users who belong to the Groups.

## Functions Applicable to Custom Roles

Functions pertinent to Custom Roles include:

* edit Custom Role name

* enable/disable Role

* enable/disable the option to have all new Users automatically added to the Custom Role

* add/remove Users from the Custom Role

* add/remove Groups from the Custom Role

## Features

**Features** are ALM objects to which you can apply privileges in the context of defining a Custom Role. Features include:

**API Token**: All endpoints are controlled by a User’s authentication token set, which is used to obtain a Bearer token for further processing. User access to the API Token feature in the ALM application will allow creation, management, and visibility of API Tokens.

**Audit**: Provides a stored log of events that occur within the ALM service. Audit records include user actions within ALM, ALM system events, and remote worker activity.

**Configuration**: Ability to define the System Administrator’s email address.

**Directory-Service**: Configuration of the Active Directory Service. This includes the External Domain, External Groups, External Users, External Group Mapping, and External OU’s.

**Email Notification**: ALM provides a set of stock Email Notification Categories. The Email Notifications alert various Users and Groups about changes and events affecting objects with which they have a connection.

**Group**: A Group is a population of Users. Groups can be configured by the customer to manage the Group’s population within ALM. Groups can be assigned to Approval Steps and Account Ownership.

**Managed Account**: Service Accounts that are created and managed through ALM.

**Provision Approval**: A specific User Role responsible for Reviewing and Approving account Requests made by Requesters. A User with Approval rights will be provided access to the Approvals screen in ALM which lists all Requests awaiting an Approver’s Review. The Approver will be able to see all the details of the Request to make their Approval decision.

**Provision Template**: Users with the ability to Provision Templates can create Workflow Templates. Workflow Templates are used to define the parameters of the accounts that will be provisioned against the Workflow Template.

**Provision Template Workflow**: Permission to Provision Template Workflow allows the User to define the Approval Steps required for an account to be Approved that has been Requested against the Workflow Template. Defining Approval Steps involves prescribing Users and/or Groups to Approval Step(s) required to be passed for the account to be provisioned for the Request.

**Remote Worker**: ALM provides users with the permissions to download the Remote Worker installer. Client-side installed Remote Workers are listed and can assigned to Remote Worker Pools within ALM.

**Role**: Roles in ALM allow users to assign Users to a specific Role or create Custom Roles. Standard Roles are Requester, Approver, and System Administrator.

**User**: A standard user within ALM will hold one of two Roles, Requestor or Approver, as described above. Users with permissions to the User feature will have the ability to add, remove, or update User accounts.

**Vault**: Configuration and management of the Thycotic Secret Server connection to ALM.

**Webhook**: Webhooks provide the ability to tie ALM to an external service. ALM provides the ability to Users with permissions to create additional custom webhooks for their business needs.

## Permissions

Permissions confer abilities to take actions within ALM. Distinct permissions within ALM include:

**Create**: Ability for role to create a certain features (e.g. Create a managed account)

**Read**: Permission to read various features displayed (e.g. Ability to read and have access to the Managed Accounts page of ALM)

**Update**: API operation type that allows change to items for their respective feature.

**Delete**: Ability to delete items for their respective feature.

**Manage**: Acts as a modifier to indicate that the role allows admin access to a respective feature. This will vary from feature to feature on how items can be managed, e.g. if the role has Manage permissions on the directory-service feature, this would allow the role to perform manual synchronization on Active Directory Objects.

![Article End](../alm-bug.png)
