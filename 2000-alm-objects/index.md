[title]: # (ALM Objects)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (2000)

# ALM Objects

ALM relies on four fundamental object types to provide governance over service accounts: Users, Roles, Groups, and Workflow Templates.

## Users

An ALM **user** object is an ALM proxy for either a **user account** or a **service account** that is **stored in Active Directory**.

* When the ALM user object is a proxy for an Active Directory **user account**, you will perform ALM operations on the ALM proxy purely to control what a person authenticated as that AD user account can do within ALM.

* When the ALM user object is a proxy for an Active Directory **service account**, you will perform ALM operations on the ALM proxy to deliver lifecycle management of the proxied AD service account.

* When you use ALM to create an ALM user object as a proxy for an Active Directory service account that **does not yet exist** in Active Directory, **ALM will create the service account in Active Directory**.

* **Except to cause this initial creation** of a service account in Active Directory, ALM operations performed on ALM proxies for AD accounts have **no effect** on the AD accounts as stored in Active Directory.

## Roles

An ALM **Role** object exists to define the ALM privileges appropriate for a particular kind of ALM user, given the tasks that kind of ALM user will perform in ALM.

* ALM Roles have **nothing to do** with Active Directory Roles and should not be confused with them.

Thycotic provisions ALM with several roles already set up—Requester, Approver, and System Administrator—and for most organizations these will suffice for initial operations.

### Requester

People in this role request provisioning of service accounts and lifecycle management for same. Requesters begin each request by selecting a Workflow Template, the specific details of which will drive the rest of request and approval process. The template also controls the specifics of the options selectable for lifecycle management to be applied to the account.

### Approver

ALM delivers requests to Approvers according to the workflow and approval steps specified by the template. An Approver receives notices of account requests and takes steps to approve or deny each request, all in conformance with the given workflow; more than one Approver may need to participate for some accounts.

On approval, ALM provisions the account and designates the Requester as the first owner.

### System Administrator

This role holds all privileges. Organizations use this all-powerful role to perform initial customer configurations of Account Lifecycle Manager. A System Administrator can provision users, integrate ALM with external systems, set up Remote Workers, and create Workflow Templates.

Because the System Administrator role is so highly privileged, its use carries risk of accidental macro-scale changes to your ALM configuration. As a best practice, use the System Administrator role only for tasks that require its privileges, and when done with those tasks, log out and resume use of less privileged roles.

### Custom Roles

Once familiar with ALM, you may decide to use the [Custom Roles](custom-roles.md) feature to create roles that support specific business needs.

* An example would be an Auditor role, configured with privileges required to view ALM’s Audit Logs but otherwise lacking the full range of privileges given to a System Administrator.

## Groups

An ALM **Group** object defines groups of ALM user objects that have something in common with each other, such as access to a resource.

* ALM Groups have **nothing to do** with Active Directory Groups and should not be confused with them.

## Workflow Templates

An ALM **Workflow Template** defines a workflow applicable to requests **made in ALM** for provisioning **in Active Directory** of a service account of a particular type.

* The Workflow Template defines the information that must be provided with the request, the approval steps that must be completed for the request to be granted, and who has approval authority at each step.

* Requests for some kinds of service accounts may require just one step, approved by only one person. Requests for other kinds of service accounts may require multiple steps and approvals by more than one person at some or all of the approval steps.

* Workflow templates also control the selection of BEOL (before end of lifecycle) and AEOL (at end of lifecycle) Notifications ALM sends, when it sends them, and to whom, plus what options the Notifications will offer for managing the service account.

![Article End](../alm-bug.png)

  

  
