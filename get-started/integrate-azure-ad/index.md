[title]: # (Integrate Azure AD)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,Azure, Azure AD)
[priority]: # (5140)

# Integrate ALM with Azure Active Directory

Use these steps to integrate ALM with Azure Active Directory:

Navigate to External Domains > Add Domain.

1.	Select Azure Active Directory in the left-hand navigation, then select App registrations under Manage.

2.	Select New registration. On the Register an application page, set the values as follows.
a.	Set Name: (Thycotic ALM)
b.	Set Supported account types to: Accounts in this organizational directory only – (Single tenant)
c.	Leave Redirect URI empty.

![Workflow Process](images/azAD_2.png)

3.	Select Register. On the Thycotic ALM App Registration page, copy the value of the Application (client) ID and (tenant) ID and save it
 

4.	Select the Add a Redirect URI link. On the Redirect URIs page, locate the Add Platform and select (Mobile and  desktop applications) section. Select the https://login.microsoftonline.com/common/oauth2/nativeclient URI. Click Configure.
 
 

5.	Locate the Default client type section and change the Treat application as a public client toggle to Yes, then choose Save. 
a.	(same screenshot as step 4)

6.	Select Certificates and secrets
a.	Click new client secret and name whatever (ALM)
b.	Copy the client secret for later
 

7.	Select API Permissions in the Left Nav
    a.	Select Add Permissions
    b.	Select Microsoft Graph
    c.	Add following permissions:
        i.	Delegated Permissions
            1.	Directory.AccessAsuser.All
        ii.	Application Permissions
            1.	Domain.ReadWrite.All
            2.	Group.Read.All
            3.	Group.ReadWrite.All
            4.	Group.Selected
            5.	User.Read.All
            6.	User.ReadWrite.All
 
8.	Select Grant admin consent
a.	Grant consent

9.	Switch over to ALM and enter the client, secret, and tenant ID in the created Azure AD Domain
 
