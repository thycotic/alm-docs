[title]: # (Integrate ALM with Secret Server)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (5305)

### Integrate ALM with Secret Server

ALM integrates with Secret Server for storage and management of account credentials, connecting to Secret Server through the Remote Worker service, which uses the Secret Server Rest API.

The minimum supported version of on-premises Secret Server is **10.2.000018**.

To integrate ALM with Secret Server, use these steps:

* In ALM, navigate to **Integrations** and select **Create Vault**.

* Use the drop-down to select the **Template type**.

* Enter your organization’s **Secret Server Instance Name**, **Secret Server URL**, and the **Account Username** and **Password** for the AD account that will run this integration.

* The **Active Directory Domain** is optional. Supply it only when using an AD account for Secret Server authentication.

The Secret Server Account used for the integration must have access to at least one folder in Secret Server, permission to create Secrets in that folder, and permissions for View Secret Template:

* View Templates

* View Folders

* Stub

* Create/Delete Secret permissions on specific folders

* Generate password based on the template

You must use a template with these fields:

* domain

* username

* password

* notes


