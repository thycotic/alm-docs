[title]: # (Create ALM Users)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5170)

# Create ALM Users

Because ALM originates in the Thycotic cloud, each member of your organization who will use ALM must have two distinct accounts.

## Thycotic One accounts

Each member of your organization who will use ALM must have a **Thycotic One** account. These free accounts provide authentication to Thycotic’s cloud services, including ALM.

To open a Thycotic One account, visit [Thycotic One](https://login.thycotic.com/Account/Login).

The email a User submits when signing up for Thycotic One will be the email they must provide later when obtaining an ALM User account.

## Steps to Create ALM Users

You set up ALM User accounts entirely within your ALM provision. Unlike Thycotic One accounts, which are not specific to ALM, ALM User accounts exist only within ALM.

Thycotic refers to ALM accounts and the people who use them as “Users,” without distinction.

* To create ALM User accounts for your organization’s members, go to **Users \> Create User**.
* Assign a **Display Name** and set the User’s **Email Address**.
* The email address should match the one used to open the User’s Thycotic One account.
* Add the User to ALM Groups, as appropriate for the User.
* **Save** the new User record.

Continue until you have created the ALM Users that enable your organization’s use cases.

Note that:

* All ALM Users automatically belong to a built-in Group called **Everyone**.
* The built-in Role called **Account Owner** cannot be removed from the **Everyone** Group.
* Accordingly, all ALM Users have the Account Owner Role.
* An Account Owner can read and update Accounts that the User has been assigned, that is, Accounts for which they are the Account Owner.

## Import Existing Users
Domain users may be imported to ALM by System Administrators of ALM by using the Account Discovery Tool. For instructions please see this article.
