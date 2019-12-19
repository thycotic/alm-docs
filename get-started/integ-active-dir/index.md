[title]: # (Integrate ALM with Active Directory)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5130)

# Integrate ALM with Active Directory

ALM presently supports Active Directory only. Future releases of ALM may support other directory services.

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

You can control the frequency with which ALM automatically syncs, as well as schedule on-demand syncs. However, note that the soonest a job will schedule is the start of the next hour from now.

* For example, if it is presently 11:16, you cannot schedule a job for 11:30 and have it run in a quarter hour from now. Instead, the sync would run at 11:30 the next day.
* However, if it is presently 11:16, and you schedule a sync for noon, it will run about 45 minutes from now, because noon meets the requirement of no sooner than the start of the next hour from now.

## Sync Users

Within a Domain, you can identify to ALM selected AD Groups and their Child Groups that should have their Users synced to ALM and then kept in sync. This tool directly applies to the task of importing existing AD user accounts into ALM for governance.

Users within selected Groups and Child Groups will automatically receive the Account Owner Role because like all Users in ALM they will belong to the Everyone Group. Once initially synced, Users may be added to other ALM Groups and assigned additional Roles. 

Use these steps to enable **Sync Users**:

* in ALM, navigate to the **Domains** page
* select a **Domain** for which you want **Sync Users** enabled 
* on the **Manage** tab of of the **Domains** detail page,
  * use the **Actions** button
  * select **Edit**
  * locate the **Sync Users** tool (in the lower half of the **Manage** tab)
* set the **Enable Sync** toggle to **Yes**
* scroll or search from the **Available Groups** table to locate which of the Domain’s Groups you want synced into ALM
* when you locate the desired Group, use the green **+** (plus) icon to the right of the Group to place it in the **Synchronized Groups** table to the right

Review your work. To commit the configuration, return to the **Actions** button at the top of the page and select **Save**.

### Notes

* You can disable this sync at any time.
* You can control the sync schedule using the **Sync this domain** feature on the **Manage** tab of the **Domains** detail page.
* Be mindful of the number of users your selections will cause to be synced into ALM, as subscription limits apply to how many users come into ALM via this feature.
  * Navigate to the **Subscription** page of ALM to view subscription consumption figures.

