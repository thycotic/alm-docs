[title]: # (Events, Notifications, and Notification Recipients)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (8300)

# Events, Notifications, and Notification Recipients
  
---
  

| **Object**          | **Event**               | **Description**                           | **Email Notification Recipients**                                      |
|---------------------|-------------------------|-------------------------------------------|------------------------------------------------------------------------|
| **Template**        | Workflow needs approval | The template's workflow needs approval.   | System Administrators                                                  |
|                     | Published               | A template has been published.            | None, by default; Allow for System Administrators                      |
|                     | Unpublished             | A template has been unpublished           | None, by default; Allow for System Administrators                      |
|                     | De-activated            | A template has been de-activated.         | None, by default; Allow for System Administrators                      |
| **Request**         | Submitted               |                                           | None                                                                   |
|                     | Step requires approval  | Kick off a step of approval               | Approvers for step                                                     |
|                     | Approved                | All the approval steps have been approved | Requester                                                              |
|                     | Rejected                |                                           | Requester                                                              |
|                     | Queued for provisioning |                                           | None                                                                   |
|                     | Provisioned             |                                           | Requester                                                              |
|                     | Provisioning failed     |                                           | Requester                                                              |
| **Managed Account** | Ownership Changed       |                                           | Account Owners                                                         |
|                     | Requires Renewal        |                                           | Account Owners                                                         |

  
---
  
