[title]: # (Workflow Roles)
[tags]: # (Account  Manager,ALM,)
[priority]: # (5340)

### Workflow Roles

To define the approval process and manage account provisioning, requests, and approvals, ALM’s Workflow system relies on three built-in user roles:

* The **System Administrator** sets up the Workflow Templates that define the approval processes for users belonging to specific Active Directory groups, or to any of a set of Active Directory groups.

* A **Requester** uses ALM to ask for Active Directory account setup. The Active Directory group requested for the account determines which Workflow Template should apply, with the template determining the applicable approval steps and the specific approvers.

* An **Approver** uses ALM to approve (or deny) account requests.
 
