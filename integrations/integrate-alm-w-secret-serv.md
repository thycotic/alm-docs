[title]: # (Integrate Account Lifecycle Manager with Secret Server)
[tags]: # (,)
[priority]: # (1610)
## Integrate ALM with Secret Server

To setup an integration with a new application, navigate to **Integrations** on the navigation pane and click **Create Integration**.

![](images/placeholder.gif)

Select the **Template** type from the drop down and enter your organization’s **Secret Server Instance Name**, **Secret Server Url**, and the **Account Username** and **Password** for the AD account that will be used to run this integration.

The **Active Directory Domain** is optional and should only be provided when using an AD account for Secret Server authentication.

The Secret Server Account used for the integration must have the following:

* Access to at least one folder and permission to create Secrets in that folder
* View Secret Template permissions

![](images/placeholder.gif)
