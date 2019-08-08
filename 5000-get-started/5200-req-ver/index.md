[title]: # (Requirements Verification)
[tags]: # (Account  Manager,ALM,)
[priority]: # (5200)

## Requirements Verification

Several requirements apply to your organization and its IT infrastructure. These include:

* Thycotic One accounts

  Each member of your organization who will use ALM must have a **Thycotic One** account. These free accounts provide authentication to Thycotic’s cloud services.

  To open a Thycotic One account, visit *login.thycotic.com*.

  * The email a user submits when signing up for Thycotic One determines the email they must provide when obtaining an ALM user account.

* suitable browsers: ALM supports Google Chrome and Mozilla Firefox

* an Active Directory installation

  You must have an Active Directory Domain Controller on **Windows Server 2012** or later, *or* **Azure AD Domain Services** and a user account with the privileges to create an AD account for ALM to use that is privileged, itself, to create accounts in AD. ALM will authenticate to Active Directory using that account.

  ALM users creates proxies for new service accounts in ALM, and ALM replicates these in Active Directory, creating the actual service accounts.

  ALM supports only Active Directory, but future releases may support other directory services.

* a functioning Thycotic Secret Server instance

  ALM uses Secret Server to store credentials for the accounts it creates in Active Directory. This removes security risks long associated with storage of the temporary credentials for new AD accounts.

* the **Remote Worker** service

  Often initially misunderstood as an actual staff member, the Remote Worker is nothing more than a Windows Service that runs on a machine in your organization’s environment.

  In software jargon, a “worker” is a process or service running in some degree independently of the main body of software to which it belongs, and used to perform tasks the main body of software cannot perform for itself.

  In the case of ALM, the Remote Worker is a Windows Service that runs on your organization’s hardware. It manages interactions between the ALM cloud service and your Active Directory installation. It also supports ALM’s integration with your organization’s Secret Server instance.

Additional requirement details apply to the Secret Server and Remote Worker components. Both involve technical matters requiring the attention of your organization’s IT staff.

### Secret Server Requirements in Detail

If you are not using Secret Server Cloud, your Secret Server version must be Version 10.1 with the Secret Server Platinum license or the API Add-on.

Because Account Lifecycle Manager works with Secret Server through Secret Server’s web services, you must enable those services on your Secret Server instance.

Use these steps to enable the Secret Server web services:

* Log in to Secret Server as an Administrator and navigate to **Admin \> Configuration**.

* On the **General** tab, under **Application Settings**, find the entry for **Enable Webservices**.

* If the entry displays as **No**, you must change it.

* Use the **Edit** button found below the settings to reveal controls for making changes.

* Set the toggle box for **Enable Webservices** to active.

* Use the **Save** button below the settings to save the change.

* You must also set up a Secret Server account for ALM that has privileges to:

* create folders accessible to ALM users

* create Secrets in those folders

* view Secret Template permissions

### Remote Worker Service Requirements

The Remote Worker is a Windows service. It must:

* be able to reach your domain controller over LDAPS

* run on a domain controller or domain-joined machine, with

  * Windows Server 2012 or later

  * Microsoft .NET 4.7.1 or later installed

* run as an AD account with AD permissions to

* create, delete, and manage user accounts

* reset user passwords and force next-logon password changes

* read all user information

* modify the membership of a group

