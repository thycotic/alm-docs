[title]: # (Events, Notifications, and Notification Recipients)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (8300)

# Events, Notifications, and Notification Recipients
  
---
  

| **Object**          | **Event**               | **Description**                           | **Email Notification Recipients**                                      |
|---------------------|-------------------------|-------------------------------------------|------------------------------------------------------------------------|
| **Template**        | Needs Approval          | A template needs approval.                | Workflow Managers                                                      |
|                     | Workflow needs approval | The template's workflow needs approval.   | System Administrators                                                  |
|                     | Published               | A template has been published.            | None, by default; Allow for System Administrators or Workflow Managers |
|                     | Unpublished             | A template has been unpublished           | None, by default; Allow for System Administrators or Workflow Managers |
|                     | De-activated            | A template has been de-activated.         | None, by default; Allow for System Administrators or Workflow Managers |
| **Request**         | Submitted               |                                           | None                                                                   |
|                     | Step requires approval  | Kick off a step of approval               | Approvers for step                                                     |
|                     | Approved                | All the approval steps have been approved | Requestor                                                              |
|                     | Rejected                |                                           | Requestor                                                              |
|                     | Queued for provisioning |                                           | None                                                                   |
|                     | Provisioned             |                                           | Requestor                                                              |
|                     | Provisioning failed     |                                           | Requestor                                                              |
| **Managed Account** | Ownership Changed       |                                           | Account Owners                                                         |
|                     | Requires Renewal        |                                           | Account Owners                                                         |
