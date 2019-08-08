[title]: # (Integrate ALM with Secret Server)
[tags]: # (Account  Manager,ALM,)
[priority]: # (5410)

### Integrate ALM with Secret Server

ALM integrates with Secret Server for storage and management of account credentials.

To integrate ALM with Secret Server, use these steps:

* In ALM, navigate to **Integrations** and select **Create Integration**.

* Use the drop-down to select the **Template type**.

* Enter your organization’s **Secret Server Instance Name**, **Secret Server URL**, and the **Account Username** and **Password** for the AD account that will run this integration.

* The **Active Directory Domain** is optional. Supply it only when using an AD account for Secret Server authentication.

The Secret Server Account used for the integration must have:

* access to at least one folder in Secret Server

* permission to create Secrets in that folder

* permissions for View Secret Template

