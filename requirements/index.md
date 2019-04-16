[title]: # (Requirements)
[tags]: # (,)
[priority]: # (1100)
# Requirements

Account Lifecycle Manager requires:

* a Thycotic One account
* Active Directory
* Secret Server
* the Remote Worker service

You need a **Thycotic One account** to authenticate with Thycotic ALM. If you do not have an account, visit <https://login.thycotic.com>. When the site prompts for a username, please use the email address you gave when you signed up for ALM.

ALM creates accounts in **Active Directory**, so you must have access to an Active Directory domain where you can set up a privileged account with account creation permissions.

ALM uses **Secret Server** to store credentials for the accounts it creates in Active Directory, removing the security risks long associated with storing credentials for new accounts.

The **Remote Worker** runs in your environment as a Windows Service. It manages interactions between Active Directory and the ALM site, and facilitates Secret Server integration.

