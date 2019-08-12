[title]: # (Integrate ALM with Active Directory)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (5415)

### Integrate ALM with Active Directory

ALM presently supports Active Directory only. Future releases of ALM may support other directory services.

Use these steps to integrate ALM with Active Directory:

* Navigate to **External Domains \> Add Domain**.

* Enter the **Name** of your Active Directory domain.

* **Add** the domain to ALM.

After you create the Active Directory domain in ALM, you must assign it to a Remote Worker Pool:

* Browse to the **Remote Worker Pools** section.

* Select the intended Remote Worker Pool and choose **Manage Pool**.

* Use **Assign** and select the Active Directory domain to assign to the pool.

* Once you assign the domain to a Remote Worker Pool, synchronize the Groups, Organizational Units and Attributes.

* Start synchronization by managing the External Domain. Each section (**Domain Groups**, **Domain Organizational Units**, and **Domain Attributes**) will have a **Synchronization** button. Use the buttons to start the syncs.

* Depending on the size of the domains, synchronizing each may require up to 15 minutes.

