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

* Once you assign the domain to an ALM Engine Pool, synchronize the Groups, Organizational Units and Attributes.

* Start synchronization by managing the External Domain.

* Each section (**Domain Groups**, **Domain Organizational Units**, and **Domain Attributes**) will have a **Synchronization** button. Use the buttons to start the syncs.

* Depending on the size of the domains, synchronizing each may require up to 15 minutes.

## Domain Synchronization

You can control the frequency with which ALM automatically syncs, as well as schedule on-demand syncs. However, note that the soonest a job will schedule is the start of the next hour from now.

* For example, if it is presently 11:16, you cannot schedule a job for 11:30 and have it run in a quarter hour from now. Instead, the sync would run at 11:30 the next day.
* However, if it is presently 11:16, and you schedule a sync for noon, it will run about 45 minutes from now, because noon meets the requirement of no sooner than the start of the next hour from now.

