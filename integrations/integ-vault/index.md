[title]: # (Integrate with Third Party Vaults)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,vault)
[priority]: # (5151)

# Integrate ALM with Third Party Vaults

ALM integrates with Azure Key Vault and AWS Secrets Manager for storage and management of Account credentials. 

## Integrate with Azure Key Vault

Use these steps to integrate ALM with Azure Key Vault:

* In ALM, navigate to **Integrations** on the left-hand menu and click **Vaults**.
* Click **Create Vault** in the upper right-hand corner.
* On the Add Vault Modal,  select **Azure Key Vault** from the Template drop-down menu. Click **Next**.
* Fill in the required fields:
    * **Azure Key Vault Display Name** is the name that will display for the vault in ALM.
    * **Azure Key Vault URL** is the location of the vault. 
    * **ClientID** is the login name for the vault.
    * **ClientSecret** is the password for the vault.
    * **TenantID** is the tenant name of your Azure account.
* Click **Save**.

Once added, you can select Azure Key Vault as a vault option when creating Workflow Templates. Accounts created from that template will use Azure Key Vault for the storage and management of account credentials.

## Integrate with AWS Secrets Manager

Use these steps to integrate ALM with AWS Secrets Manager:

* In ALM, navigate to **Integrations** on the left-hand menu and click **Vaults**.
* Click **Create Vault** in the upper right-hand corner.
* On the Add Vault Modal, select **AWS Secrets Manager** from the Template drop-down menu. Click **Next**.
* Fill in the required fields:
    * **AWS Secrets Manager Display Name** is the name that will display for the vault in ALM.
    * **AWS Secrets Manager URL** is the location of the vault. 
    * **Access Key ID** is the login name for the vault.
    * **Secret Access Key** is the password for the vault.
* Click **Save**.

Once added, you can select AWS Secrets Manager as a vault option when creating Workflow Templates. Accounts created from that template will use AWS Secrets Manager for the storage and management of account credentials.
