[title]: # (Summary of ALM User Personas and Use Cases)
[tags]: # (Account  Manager,ALM,)
[priority]: # (8100)

# Summary of ALM User Personas and Use Cases 

ALM relies on three user personas: the Requestor, the Approver, and the System Administrator.  

## Requestor 

**User Purpose Summary**: A requestor will be any person in a business organization that requires utilization and lifecycle management of a service account. The Requestor requires the ability to submit account requests through the Account Lifecycle Manger’s approval workflow and lifecycle management model prescribed by the Administrator users in their organization. 

**User Demographic**: Requestors will hold, but not limited to such positions as Developers, IT Security Professionals, Analysts, Delivery Operations Teams, and Developer Operation Teams. 

**User Goals and Tasks**: When a Requestor has a need to setup a new service account, they will submit the account Request to Account Lifecycle Manager’s website-based application. 

**Details**: The Requestor must define in the request which Workflow Template the account is going to applied to. The selected Workflow Template will define the parameters for the account for its lifecycle. Once the Workflow Template is selected the Requestor is required to provide a justification and reasoning statement for the account being requested. The justification and reasoning statement will be reviewed by the users selected in the Workflow Template that will be reviewing the request for approval, before the account is provisioned. The Requestor must also select a Review Interval time period for the account, this is a selection of time period prescribed by the selected Workflow Template and indicate when the account needs to be reviewed by the Requestor and other selected account owners. Finally, when the Requestor is submitting the request the user is presented with what Approval Steps must be passed for the account to be provisioned. 

After an account has been approved and provisioned the account is now considered a Managed Account to the Requestor and other account owners. Account Lifecycle Manager allows the Requestor to view all their accounts on the Managed screen of the site application. The Requestor will be able to see the current status of the account at a glance, and ultimately be required to review their account when the lifecycle is nearing an end, as defined from the initial Request. When an account is available for review the Requestor will be deciding for the account to Renew, Disable, or ‘Delete the Account and Secret’. The Requestor will be provided notifications to ensure opportunity to review the account before its determined End of Lifecycle Action, as defined by the account’s associated Workflow Template. 

## Approver 

**User Purpose Summary**: An Approver will be individuals and groups of people at the business organization that provide oversight and approval to accounts being requested by the Requestors. It is the role of the Approver to confirm the justification for the accounts being requested and commit their approval. Approvers will act in various Levels of the approval process, as determined by the Workflow Template configured by the Administrator. 

**User Demographic**: Approvers will hold, but not limited to such positions as Managers within Business Units, Asset Owners, Database Administrators, App Server Administrators, Networking Administrators, and Security Teams. 

**User Goals and Tasks**: When an Approver is prescribed to an Approval Step, as defined by the Workflow Template, the Approver will be notified and presented a queue of Requests requiring Approval in the Account Lifecycle Manager’s website application. 

**Details**: An Approver will act in various Levels of Approval Steps, as defined by the Workflow Template associated the account Request. This may be an initial Level 1 Approval Step, or act as Approver in sequentially additional Level Approval Steps as defined by the Workflow Template. 

The assigned Approvers will be notified by Account Lifecycle Manager when a Request has been submitted for Approval. It is the goal of the Approver to review the Request in a timely fashion, for the Request to ultimately achieve provisioning. The Approver will either Approve the Request or Deny the Request. If the Approver Approves the Request, it will be passed to any additional Approval Steps required by the Workflow Template. If the Approver Denies the Request the Approver is asked to provide a written reason as to why the Request is Denied, which will be provided to the Requestor. 

## System Administrator 

**User Purpose Summary**: A System Administrator is an individual or group of individuals at the business organization that has permissions to define Workflows, integrate Active Directory, integrate Secret Server, and other administrative tasks. 

**User Demographic**: System Administrators will hold, but not limited to such positions as Managers within Business Units, Asset Owners, Database Administrators, App Server Administrators, Networking Administrators, and Security Teams. 

**User Goals and Tasks**: The System Administrator is responsible for initial configuration of Account Lifecycle Manager. This will include the tasks of provisioning users, integrating systems, setup of Remote Workers, and creating Workflow Templates. 

**Details**: The System Administrator is responsible for the architecture of the workflow to which accounts are managed within Account Lifecycle Manager. This task is primarily handled via the creation of the Workflow Templates. Workflow Templates allow the System Administrator to define the Terms of Service, Type of the Account, configure Active Directory, connect Secrets Vault, define the End of Lifecycle Action for accounts, define review interval time period options for the Requestor to select, define notifications types for the End of Lifecycle, and define the required Approval Steps. 

Once a Workflow Template is published the Requestor can begin submitting account Requests against the Workflow Template. When a change or modification is required of a published Workflow Template the System Administrator will have the ability to create additional versions of the Workflow Templates. Provisioned accounts will remain associated to the version of the Workflow Template that they were originally approved against. 
