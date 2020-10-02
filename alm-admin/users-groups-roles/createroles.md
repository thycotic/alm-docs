[title]: # (Create Roles)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5160)

# Use or Create Roles

**Roles** control privileges within ALM, and **only within ALM**.

* Like ALM Groups, ALM Roles do **not** correspond to any similar entities in Active Directory or any other directory system.

## Default Roles Provided by ALM

ALM supplies several default Roles, as in the following table, that your organization may find adequate or may use as models for its own Roles development.

  
---
  
| Default ALM Role     | Permissions                                      | 
|----------------------|--------------------------------------------------|
| Account Owner        | read managed Account                             |
|                      | update managed Account
| Provision Requester  | request a new Account                            |
| Provision Approver   | Approve Requests                                 |
| System Administrator | authorize all Role types                         |
|                      | create Workflow Templates                        |
|                      | set up ALM Engines                               |
|                      | perform ALM Integration with Active Directory    |
|                      | perform ALM Integration with Secret Server       |

---

## Create Custom Roles

If the default Roles do not meet your organization’s needs, you can create Custom Roles.

Role names often reference job titles, but astute ALM administrators will name ALM Roles more to suggest the **privileges** the Role confers in ALM than to describe the Role’s **duties**.

* To create new Roles, go to **Roles \> Create Role**.
* Enter a name for the new Role.
* **Add** the new Role to ALM.

## Define Role Permissions

After you add a new Role, ALM displays the **Details and Permissions** panel, which features controls used to define or adjust permissions for the Role.

* Adjust the permissions by clicking any of the CREATE, READ, UPDATE, DELETE, or MANAGE toggle boxes for each of the features.
* Unchecking one of the permissions check boxes **for a feature** will remove from **this Role** the permission to perform **that type of activity** in relation to **that feature**.
* ALM saves changes to Role permissions **as you make them**—there is no **Save** or **Apply** button.

Continue creating Roles and defining their permissions until you have satisfied the requirements for your organization’s ALM use cases.
