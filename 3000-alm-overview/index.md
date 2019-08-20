[title]: # (ALM Overview)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (3000)

# ALM Overview

ALM came from a straightforward idea—provide a cloud app’s clean design and intuitive UI as a front end to Active Directory (and in the future, other directory services), allowing administrators to more easily and efficiently request, approve, privilege, manage, and retire service accounts by delegating the Active Directory intricacies to the cloud app.

That is the essence of ALM. The tasks involved form a simple, linear workflow:

* members of the organization use Account Lifecycle Manager to **request service accounts**

* ALM **notifies the staff holding approval authority** for the requested service accounts

* those staff **receive the notifications** and use ALM to **approve or deny** the requests

* for approved service accounts, the approver (or other designated role) **creates proxies for the service accounts** in ALM

* ALM **logs in to Active Directory** using a suitably privileged service account and **creates the actual user accounts**, naming them the same as their proxies in ALM

* ALM **notifies the requester** of the account’s provisioning

* using properties assigned within ALM to the proxies of the service accounts, ALM tracks accounts to promote their timely evaluation for renewal or retirement on designated dates

These activities follow **workflows** defined by the organization using **workflow templates**. ALM logs each step to support a robust audit capacity.

