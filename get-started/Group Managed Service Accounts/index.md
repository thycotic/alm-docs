[title]: # (Integrate group Managed Service Accounts)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,Azure, Azure AD)
[priority]: # (5135)

# Integrate group Managed Service Accounts

## Overview:

Group Managed Service Accounts provide automatic password and simplified service principal name (SPN) management to multiple servers. 

ALM supports the provisioning and lifecycle management of gMSAs. This is achieved when **Group Managed Service Account** is selected as the **Account Type** when the System Administrator is creating a **Workflow Template**.

## Requirements:
* RSAT needs to be installed on the engine machine
    * Use Powershell and run script: Install-WindowsFeature RSAT-AD-PowerShell
    * Use GUI and Enable RSAT through Turn Windows Features on or off
* Microsoft Active Directory prerequisites and one-time preperation, [see Microsoft documentation](https://docs.microsoft.com/en-us/virtualization/windowscontainers/manage-containers/manage-serviceaccounts)

## Parameters:
Certain Parameters are set by default and others by the attributes list in a workflow template.
* **PrincipalsAllowedToDeleteToAccount** - Set by the Users and Groups selected in the template.
* **KerberosEncryptionType** - Accepted values (None, DES, RC4, AES128, AES256). Only one is allowed.
* **ServicePrincipalNames** - Accepts a command separated list of service principal names. This has to be unique for each request.

