[title]: # (Secret Server Requirements)
[tags]: # (,)
[priority]: # (1120)
## Secret Server Requirements

You must have Secret Server 10.1 with either the Secret Server Platinum license or the API Add-on.

Account Lifecycle Manager works with Secret Server through Secret Server’s web services, which you must enable:

* Login as an Administrator and navigate to **Admin \> Configuration**.
* On the **General** tab, under **Application Settings**, locate the entry for  **Enable Webservices**.
* If the entry displays as **No**, you must change it.

  * Use the **Edit** button located below the settings to reveal controls.
  * Set the toggle box for **Enable Webservices** to active.
  * **Save** the change using the same-named button below the settings.

You must also set up a Secret Server account for ALM that can:

* create folders accessible to ALM users
* create Secrets in those folders
* view Secret Template permissions
