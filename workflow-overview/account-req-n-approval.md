[title]: # (Account Request and Approval Workflow)
[tags]: # (,)
[priority]: # (1820)
## Account Request and Approval Workflow

User Roles Engaged:

* Provision Requester
* Provision Approver

After the provisioning process is in place through the published workflow template, Provisioning Server will be able to provision new accounts by following the template rules. A basic workflow for account provisioning follows these steps:

* A user with the Provision Requester Role can now submit a request for a new account through the Workflow Template that was created by the System Administrator in the previous section.
* Once this account request is submitted, Provision Approvers will be notified of the request in order that is defined by the Approval Workflow created by the Workflow Manager in the previous section. Assigned approvers will sign off on the request or reject the request.

Once all approval conditions are met, Thycotic Account Lifecycle Manager will automatically spin up the requested account and then generate a corresponding Secret inside of Secret Server so that the new account credentials can be effectively managed through the Secret Server vault as long as this account exists.
