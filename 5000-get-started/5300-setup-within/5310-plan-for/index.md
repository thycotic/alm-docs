[title]: # (Plan for Groups, Roles, and Users)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (5310)

### Plan for Groups, Roles, and Users

Management of privileges within ALM, to control ALM’s own system of user privileges, relies on easily grasped permissions constructs—notions of read, read-write, list, and so forth—recognizable by anyone familiar with file system permissions.

Additionally, ALM uses familiar objects like users, groups, and roles—so setting up your organization’s ALM user permissions should require little consideration. However, a critical caveat applies.

* It is important to understand that while ALM replicates its user objects in Active Directory, such that there will be a one to one correspondence between ALM user objects and Active Directory user objects, **nothing similar to this** applies to ALM group objects.

>   ALM does not create Active Directory groups, and no equivalency of function >   exists between ALM groups and AD groups.

To manage ALM user privileges within ALM, you can add ALM users to ALM groups, and then either or both of these entities to ALM roles.

An ALM user object’s membership in an ALM Group or Role has zero impact on Active Directory, allowing you to make dual use of the ALM user objects—they represent enterprise user accounts in AD, while also functioning as ALM user accounts with privileges managed within ALM.

#### ALM Objects are Objects Forever

When you create an ALM object, you create it forever—ALM does not support deleting objects, whether users or roles or another type. However, you can disable any object.

