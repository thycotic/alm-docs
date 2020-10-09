[title]: # (Create and Manage Roles)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5160)

# Create and Manage Roles

**Roles** control privileges within ALM. To access the Role page, click **Personnel** in the left-hand menu and then click **Roles**.

![rolesnav](images/roles-nav-menu.png)

## Default Roles Provided by ALM

ALM supplies several default Roles, as in the following table, that your organization may find adequate or may use as models for its own Roles development.

> **Note**: Like ALM Groups, ALM Roles do **not** overlap with roles in Active Directory or other directory systems.

---
  
| Default ALM Role     | Permissions                                      | 
|----------------------|--------------------------------------------------|
| Account Owner        | Read managed Account                             |
|                      | Update managed Account
| Provision Requester  | Request a new Account                            |
| Provision Approver   | Approve Requests                                 |
| System Administrator | Authorize all Role types                         |
|                      | Create Workflow Templates                        |
|                      | Set up ALM Engines                               |
|                      | Perform ALM Integration with Active Directory    |
|                      | Perform ALM Integration with Secret Server       |

---

## Create Custom Roles

You can create custom Roles to further control access within ALM. 
To create a new Role

1. Click **Create Role** in the upper right-hand corner of the Role page.
1. Enter a **Name** for the new Role and click **Add**.
1. Click **Add** to bring up the **Manage Role** page.

    ![manageroles](images/roles-management.png)

1. On the Manage Role page, assign permissions to the Role by checking the boxes next to the privileges the Role should have within ALM. **Settings will update as you check the boxes. You will not need to click apply or save.**
1. Scroll to the bottom of the page and click **Add user** to bring up a list of available Users. Check the boxes next to the Users to assign to the Role and click **Add**.

    ![adduser](images/groups-add-users-window.png)

1. Underneath Add user, click **Add group** to bring up a list of available Groups. Check the boxes next to the Groups that should include the Role and click **Add**.

## Manage Roles

Open the Role Management page by clicking on the name of the Role to be managed.
> **Note**: If you cannot find the Role you wish to manage, you may be viewing only enabled Roles. To filter Roles by All/Enabled/Disabled, click the **Status** drop-down and select the correct option.

![manageroles](images/roles-management-entry.png)

### Change Role Permissions

* On the Manage Role page, assign permissions to the Role by checking the boxes next to the privileges the Role should have within ALM. **Settings will update as you check the boxes. You will not need to click apply or save.**

### Enable/Disable Role

* Click **disable** on the right side of the screen to disable the Role. Disabling will **not** delete the Role.
* Click **enable** on the right side of the screen to activate the Role and restore permissions to Users with the Role's permissions.

### Automatically Apply to new Users

* Enabling **Automatically apply to new users** will assign this Role to **all** newly created Users. If you choose this option, **make sure that the permissions you give this Role are limited.**
