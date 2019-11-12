[title]: # (Custom Roles)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (2100)

# Custom Roles

ALM System Administrators can create Custom Roles. To define Custom Roles, you review a list of ALM features paired with the permissions potentially applicable to each feature.

* Roles differ from one another in the specific permissions assigned to them in relation to each ALM feature.

* A Custom Role is a Role you create to meet your specific business needs when the built-in Roles will not suffice.

Once you have set the per-feature permissions for a Role, you add Users or Groups (or both) to the Role, thereby granting the Role’s permissions to those Users, and to Users who belong to those Groups.

As with the built-in Roles, you can:

* edit the name of the Custom Role
* enable or disable the Custom Role
* enable or disable automatic addition of new Users to the Custom Role
* add or remove Users from the Custom Role
* add or remove Groups from the Custom Role

## Permissions

Permissions control what actions Users can take within ALM. Distinct permissions within ALM include:

**Create** allows creation of the object for which you grant the permission

**Read** allows passive use of a feature, such as to read (view) a list of objects or view an object’s details

**Update**: allows changes to the object for which you grant the permission, for example, update a Managed Account

**Delete**: allows a User to delete the object for which you grant the permission

**Manage**: gives additional, administrative access to the object to which it applies, for which the User must already have non-administrative privileges

* As an example, Users with Manage permissions on the Directory-Service feature can perform manual synchronization on Active Directory Objects.

## Features to Which Permissions Apply

In defining a Custom Role, you specify the permissions the Custom Role holds in relation to specific ALM features. The features subject to access control via permissions include:

**API Token**: Access to the API Token feature allows a User to view, create, and manage API Tokens. These enable the User to obtain Bearer tokens, required by ALM for further processing.

**Audit**: ALM logs most events, including User actions, system events, and remote worker activity. Audit permissions allow a User to view these logs.

**Configuration**: A User with Configuration permissions can define the System Administrator’s email address.

**Directory-Service**: With Directory Service permissions, a User can configure ALM’s integration with the organization's directory services provider—its **External Domain**:

* Presently ALM supports only one External Domain, that being Active Directory.
* For Active Directory, additional setting include AD Groups, Users, Group Mappings, and OUs.

**Email Notification**: ALM provides several broadly applicable Email Notification Categories. Email Notifications inform Users and Groups of Users about events affecting objects with which they have a connection—for example, the User is named in the governing Workflow Template as the Approver for a step in the workflow.

**Group**: Groups are collections of Users. You use Groups to more efficiently apply the same management activities to more than one User at once. You can assign Groups to Approval Steps just as you would an individual User; likewise you can assign Account Ownership to a Group.

**Managed Account**: A Managed Account is an AD Service Account created and managed through ALM.

**Provision Template**: With Provision Template permissions, Users can create Workflow Templates to govern the approval process for AD service accounts.

**Provision Template Workflow**: Provision Template Workflow permissions allow a User to set a Workflow Template’s Approval Steps. Setting Approval Steps involves designating which Users and Groups must approve the provisioning of a requested service account, and in what order—the workflow.

**Provision Approval**: To be designated as an Approver for Approval Steps set in a Workflow Template , a User must have permissions for Provision Approval. This gives access to ALM’s Approvals section, which lists Requests waiting for an Approver’s review and gives access to all Request details.

**Remote Worker**: A User must have Remote Worker permissions to download the installer for the Remote Worker Windows Service. This permission also enables the User to view in ALM the list of installed Remote Workers and assign Remote Workers to Remote Worker Pools.

**Role**: The Roles permission enables a User to create Custom Roles and assign Users to them. It also allows the User to add Users to the standard Requester, Approver, and System Administrator Roles.

**User**: Users with permissions to the User feature can add, remove, or update User accounts, including to designate whether a User is an Approver or Requester.

**Vault**: With Vault permissions, a User can configure and manage ALM’s connection to your organization’s Thycotic Secret Server.

**Webhook**: Webhooks provide a framework for connecting ALM to external services. With Webhooks permissions, a User can create custom webhooks.

The [Example Custom Roles Setup](custom-roles-ex-table.md) article details permissions for a broadly useful Custom Roles setup.
