[title]: # (Events, Notifications, and Recipients)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,AEOL,BEOL,End of Lifecycle,Before End of Lifecycle,)
[priority]: # (2200)

# Events, Notifications, and Recipients

To request that a new AD service account be provisioned, a Requester selects the Workflow Template applicable to the type of service account being requested, provides the information required by that Workflow Template, and submits the Request.

From there, the Request must pass through each of the Approval Steps specified by the Workflow Template. As this happens, ALM keeps process participants informed by sending Notifications. If the Request wins approval, the service account will be provisioned.

Provisioning marks the beginning of the account’s lifecycle—the period of time it remains active, during which it will be tracked according to the specifications in the Workflow Template against which it was provisioned.

* For example, the template might specify that the account should expire in one year; or, that it requires renewal after six months. ALM sends notifications timed in relation to these settings—if an account requires renewal at six months, ALM notifies the account owner in advance of the six-month mark. Within ALM, the account owner has the option to approve or deny account renewal.

ALM provides for varied and strongly granular lifecycle event tracking and notification activities, as in the following table.

**Table:** *Account Lifecycle Manager Events, Notifications, and Recipients*

| **Object**          | **Event**               | **Description**                                   | **Email Notification Recipients**                 |
|---------------------|-------------------------|---------------------------------------------------|---------------------------------------------------|
| **Template**        | Workflow needs approval | The template's workflow needs approval.           | System Administrators                             |
|                     | Published               | A template has been published.                    | None, by default; Allow for System Administrators |
|                     | Unpublished             | A template has been unpublished                   | None, by default; Allow for System Administrators |
|                     | De-activated            | A template has been de-activated.                 | None, by default; Allow for System Administrators |
|                     |                         |                                                   |                                                   |
| **Request**         | Submitted               | A Requester asks that an account be provisioned.  | None                                              |
|                     | Step requires approval  | Kick off a step of approval                       | Approvers for step                                |
|                     | Approved                | All the approval steps have been approved         | Requester                                         |
|                     | Rejected                |                                                   | Requester                                         |
|                     | Queued for provisioning |                                                   | None                                              |
|                     | Provisioned             |                                                   | Requester                                         |
|                     | Provisioning failed     |                                                   | Requester                                         |
|                     |                         |                                                   |                                                   |
| **Managed Account** | Ownership Changed       |                                                   | Account Owners                                    |
|                     | Requires Renewal        |                                                   | Account Owners                                    |

---
Closely related to these notifications, ALM [At End of Lifecycle Actions (EOLAs)](eol-actions.md) define the actions Account Owners can take when an account expires, for example, they can renew the account. Similarly, **BEOLs** refers to Before End of Lifecycle Actions, the steps Account Owners can take when an account nears its expiration date.


