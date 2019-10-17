[title]: # (Overview)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (1000)

# Overview

ALM came from a straightforward idea—provide a cloud app’s clean design and intuitive UI as a front end to Active Directory (and in the future, other directory services), allowing enterprise IT users to more easily and efficiently request, approve, privilege, manage, and retire service accounts by delegating the Active Directory intricacies to the cloud app.

That is the essence of ALM. The tasks involved form a simple, linear workflow:

* Members of the organization use Account Lifecycle Manager to **request service accounts**.

* ALM **notifies the staff holding approval authority** for the requested service accounts.

* Those staff **receive the notifications** and use ALM to **approve or deny** the requests.

* For denials, the approval authority records the reasons for the denial, and ALM notifies the requester of the denial and the reasons given.

* For approvals,

  * The approver (or other designated role) **creates proxies within ALM for the requested Active Directory service accounts**.

  * ALM **logs in to Active Directory** using a suitably privileged service account and **creates the actual AD user accounts**, naming them the same as their proxies in ALM.

  * ALM **notifies the requester** of the account’s provisioning in Active Directory.

Once a service account has been provisioned, ALM monitors the account throughout its lifecycle:

* Using ALM properties assigned within ALM to the ALM proxies of the Active Directory service accounts, ALM tracks service accounts after their creation—promoting their timely evaluation for renewal or retirement by designated dates.

* ALM’s tracking relies on a system of Notifications and adherence to **workflows** defined by **Workflow Templates** created by the organization.

* For each customer-designated category of service accounts, an ALM Workflow Template determines which BEOL (before end of lifecycle) and AEOL (at end of lifecycle) Notifications ALM sends, when, and to whom, plus what options the notified party has for managing the account.

ALM’s Workflow Templates support its straightforward customization to fit each organization’s particulars.

ALM logs each step to support a robust audit capacity.
