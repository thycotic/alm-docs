[title]: # (Active Directory Account Discovery Tool)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5135)

# Active Directory Account Discovery Tool

The AD Account Discovery Tool allows System Administrators to select any or all service Accounts within a specific domain and import them to ALM, where they can be managed by aassociating them with Workflow Templates and assigning Owners.

Located under Administration > Account Discovery, the tool presents a simple four-step process for bringing AD service Accounts under ALM management.

**Be sure to familiarize yourself** with the limitations on these steps before you begin this process.

* select the domain
  * limit: you can select only **one** domain at a time; to analyze multiple domains, you must separately apply the Discovery Tool to each domain
* select Accounts within the domain
  * note: Accounts must be selected from Organizational Units; you *can* select Accounts from multiple OUs
* assign the selected Accounts to *a* Workflow Template
  * limit: you will only have the option to assign **all** of the selected Accounts to **one** Workflow Template
* assign Users and Groups as Owners of the Accounts
  * limit: in assigning Users and Groups to be the Account Owners, you will be assigning **all** of the Accounts you selected to be owned by **each** User and Group you select here
