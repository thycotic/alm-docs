[title]: # (Build Workflow Templates)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5190)

# Build Workflow Templates

To use ALM, you must define the approval processes your organization intends to apply to Requests for different kinds of service accounts. Some types of service accounts might be approved and provisioned on Request, while others might need more than one Approval before provisioning.

## Overview

ALM supplies a straightforward, Roles-driven workflow system to support your oversight of new AD account creation, review, and eventual renewal or retirement.

ALM represents your approval processes as Workflow Templates. Each template defines the approval process for a particular service account kind or category as defined by your organization—for example, service accounts belonging to specific Active Directory Groups.

As illustrated, ALM’s workflow system follows a simple, linear process from template definition through account Requests and Approvals.

![Workflow Process](images/workflow-process.png)

## Create a Workflow Template to Define a Workflow

Use this procedure to create the Workflow Templates necessary to support your organization’s use cases. You must have the System Administrator Role to perform this procedure, and you must have already connected ALM to your Secret Server.

* Navigate to **Administration** in the menu, select **Workflow Templates**
* Use the **Create Template** button (upper right of the page) to open the **Workflow Template Wizard**.
* Supply a name for the template.
* Select the **Account Type**.
  * Active Directory
  * Azure Active Directory
  * Group Managed Service Account
* Supply the **Terms of Service** (*optional*)
* Define the **Purpose** of the Workflow Template.
* Connect the **Secrets Vault**.
* Set up the **Active Directory**.
* Choose the **End of Lifecycle Action** for accounts based on this template:
  * Review
  * Disable
    * Note: Allows for the optional setting to select an Organization Unit (OU) for the account to be sent to automatically when the account is Disabled by ALM at the end of its determined lifecycle. 
  * Expire
  * Delete
* Define the **Review Intervals** available to the Requester.
* Choose **Notification Options**:
  * Before End of Lifecycle Notifications
  * On/After End of Lifecycle Notifications
* Define the **Approval Steps**.
  * Add **Approvers** to at least one Approval Step. You can add individual Users, or Groups thereof.
* Publish the completed Workflow Template.

## Workflow Administration



The **Workflow Template Versioning** feature allows System Administrators to make changes to an already published Workflow Template, instead of creating an entirely new Workflow Template and disabling the previous one.

* The Administrator opens the Template and selects **Create New Version**.
* ALM will prompt for confirmation that the System Administrator wants to create a new version of the Workflow Template.
* When a new version of a Workflow Template is created and then Published, all new Account Requests will provision against the latest Published version.
* All accounts previously provisioned to prior versions will remain associated to the version they were provisioned against.

Users with permissions to access Workflow Templates will be able to view the specification of previous versions for change tracking. The Managed Accounts view will display which version of a Workflow Template the account is provisioned against.