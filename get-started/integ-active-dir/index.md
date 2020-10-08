[title]: # (Integrate ALM with Active Directory)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5130)

# Integrate ALM with Active Directory

Use these steps to integrate ALM with Active Directory:

* Navigate to **External Domains \> Add Domain**.

* Enter the **Name** of your Active Directory domain.

* **Add** the domain to ALM.

After you create the Active Directory domain in ALM, you must assign it to an ALM Engine Pool:

* Browse to the **ALM Engine Pools** section.

* Select the intended ALM Engine Pool and choose **Manage Pool**.

* Use **Assign** and select the Active Directory domain to assign to the pool.

Once you assign the AD domain to an ALM Engine Pool, you start synchronization by managing the External Domain.

To perform an ad-hoc synchronization of a specific Domain, go to the **Manage** tab of the Domain, use the **Actions** button, and select **Sync**.

* the Users, Groups, Organizational Units, Attributes, and Managed Accounts of the Domain will all be synced

* depending on the Domain size, synchronizing may take up to 15 minutes

## Domain Synchronization

You can set the interval that ALM automatically syncs and schedule on-demand syncs.

> Note: ALM checks for synchronization requests at the top of each hour. Syncs should be scheduled for the start of the next hour or they will not start until the following day. *Example: If it is 9:30, the soonest a sync can be scheduled is 10:00. If a sync were scheduled at 9:30 for 9:45, ALM Would not sync until 9:45 the following day.*

## Sync Users

Within a Domain, you can identify to ALM selected AD Groups and their Child Groups that should have their Users synced to ALM and then kept in sync. This tool directly applies to the task of importing existing AD user accounts into ALM for governance.

Users within selected Groups and Child Groups will automatically receive the Account Owner Role because like all Users in ALM they will belong to the Everyone Group. Once initially synced, Users may be added to other ALM Groups and assigned additional Roles. 

Use these steps to enable **Sync Users**:

1. Navigate to the **Domains** page
1. Select the **Domain** to **Sync Users**.
1. On the **Manage** tab of of the **Domains** detail page,
    1. Click **Actions** 
    1. Select **Edit**
    1. In the lower half of the **Manage** tab, locate the **Sync Users** tool.
1. Set the **Enable Sync** toggle to **Yes**
1. Scroll or search from the **Available Groups** table to locate the Domain’s Groups to sync with ALM.
1. Click the green **+** (plus) icon to the right of the Group to place it in the **Synchronized Groups** table on the right.
1. To finalize the configuration, return to **Actions** at the top of the page and click **Save**.

### Notes

* You can disable this sync at any time.
* You can control the sync schedule using the **Sync this domain** feature on the **Manage** tab of the **Domains** detail page.
* Be mindful of the number of users your selections will cause to be synced into ALM, as subscription limits apply to how many users come into ALM via this feature.
  * Navigate to the **Subscription** page of ALM to view subscription consumption figures.
