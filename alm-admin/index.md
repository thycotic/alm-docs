[title]: # (Administration)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (6000)

# ALM Administrative Tasks

Some operations will be performed only occasionally, for example, managing Roles or administering Workflows.

## Manage Roles

ALM automatically enables newly created Roles.

To enable or disable a Role:

* Go to **Roles \> [Select Role] \> Manage Role**.
* Use **Edit** to adjust the name of the Role.
* Use **Enable** or **Disable** to recommission or decommission a Role, respectively.

## Manage Groups

On the **Manage Groups** page you can edit the Group name, disable or enable the Group, and add Users and Roles to the Group.

* To add a User to the Group, click **Add User**.
* Enter search criteria.
* Select a User from the list of results.
* Click **Add**.

## Manage Users

On the **Manage User** page you can

* edit the User **Display Name**
* disable or enable the User
* add an email address
* assign the User to Groups and Roles

## Workflow Administration

The UI used to [create Workflow Templates](../get-started/build-workflows/) also supports updating them.

The **Workflow Template Versioning** feature allows System Administrators to make changes to an already published Workflow Template, instead of creating an entirely new Workflow Template and disabling the previous one.

* The Administrator opens the Template and selects **Create New Version**.
* ALM will prompt for confirmation that the System Administrator wants to create a new version of the Workflow Template.
* When a new version of a Workflow Template is created and then Published, all new Account Requests will provision against the latest Published version.
* All accounts previously provisioned to prior versions will remain associated to the version they were provisioned against.

Users with permissions to access Workflow Templates will be able to view the specification of previous versions for change tracking. The Managed Accounts view will display which version of a Workflow Template the account is provisioned against.

## Remote Worker Calibration

ALM’s **Remote Worker Calibration** tool automatically determines which of your Remote Workers can access what Vaults and which External Domains (Active Directory domains).

To use the Remote Worker Calibration tool:

1. Go to the **Vaults** page.
2. Select the Vault for which you need an active Remote Worker connection to be established.
3. On the **Vault Details** page, go to the **Remote Workers** tab.
4. Click **Calibration**.

This will queue a **Remote Worker Calibration Job** and prompt a modal dialog stating:

* Remote Worker Calibration started, this may take several minutes to complete.

The Remote Worker Calibration Job connects with the Remote Workers, tasking each one to authenticate with the Secret Server Vault you selected. The Calibration Job keeps track of which Remote Workers successfully authenticate to the Vault, creating a list of Remote Workers known to have access to that Secret Server.

* That list populates a table on the Remote Workers tab of the Vault Details page.
* Remote Workers that did not authenticate will not appear on the list.
* If no Remote Worker authenticated, the Vault Details page will indicate that “No Remote Workers calibrated to integration.”

A Remote Workers Calibration Job runs as part of any Scheduled Sync for a Vault, with the list of successfully authenticating Remote Workers updating on completion of the sync job.
