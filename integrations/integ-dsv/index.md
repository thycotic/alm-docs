[title]: # (Integrate with DevOps Secrets Vault)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,DevOps Secrets Vault,DSV)
[priority]: # (5150)

# Integrate ALM with DevOps Secrets Vault

ALM integrates with Thycotic’s DevOps Secrets Vault (DSV) for storage and management of Account credentials. 

Use these steps to integrate ALM with DevOps Secrets Vault:

* in ALM, navigate to **Vaults** and select **Create Vault**
* a modal pane will appear; open its **Template** drop-down and select *Thycotic DevOps Secrets Vault*
* use **Next** to confirm that selection; then fill in the information it requires:
  * the **Thycotic DevOps Secrets Vault Display Name** entry is the vault label in ALM that distinguishes it from other vaults 
  * the **DevOps Secrets Vault URL** specifies the URL of your DevOps Secrets Vault instance 
  * the **ClientID** records the Client ID of your DevOps Secrets Vault instance
  * the **ClientSecret** is the password for your ClientID
* use **Save** to confirm your entries 

Once you have added it, you can select DevOps Secrets Vault as a vault option when creating Workflow Templates.

* Requests made based on Workflow Templates that have a DevOps Secrets Vault will use DevOps Secrets Vault for the storage and management of Account credentials. 


