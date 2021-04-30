[title]: # (Release Notes)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (8450)

# Release Notes

As a cloud application updates become available to all Users as they occur—the current version is always the only version available. Thycotic periodically updates Account Lifecycle Manager to introduce additional features and provide fixes and improvements.

This article tracks those changes to ALM.

## Account Lifecycle Manager: Change Log

| **Update**             | **Notes**                                                                                                                                                           |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| May 2021               | feature: ALM now integrates with HashiCorp Vault.|
||
| April 2021             | improvement: Minor enhancements and improvements.|
||
| March 2021             | feature: ALM now integrates with Azure Key Vault and AWS Secrets Manager.|
|                        | improvement: UI updates throughout ALM.|
||
| February 2021          | feature: The [Account Migration](./alm-admin/migrate.md) page allows administrators to change the workflow template, review interval, lifecycle end date, and owners of an existing service account. 
|                        | improvement: Workflow templates include the option to hide the names of approvers from requesters.|
|                        | improvement: Workflow templates include the option to allow a requester to choose sub-organization units within a designated folder.|
|                        | improvement: Webhooks can now be tested from the Webhook Management page.|
||
| January 2021           | feature: The [SIEM integrations](./integrations/integ-siem/index.md) page allows administrators to integrate ALM with SIEM applications.| 
|                        | improvement: Updated UI for webhook authorization, workflow templates, account discovery, and custom HTTP headers.|
|                        | improvement: Administrators can specify the maximum number of service account owners when creating a template.|
|                        | 
| December 2020          | feature: The [webhook authorization](./alm-admin/alerts.md) page allows administrators and users with webhook permissions to add authentication to webhooks.|
|                        | improvement: Administrators and users with webhook permissions can add custom HTTP headers to webhooks.|
|                        | improvement: When creating or editing an Active Directory template, administrators can restrict users from changing passwords.|
|                        | improvement: When creating a workflow template, administrators can define a regex check on Service Account names.|
|                        | improvement: When a Secret Server vault sync is run, ALM will search for managed accounts without a SecretID.|
|                        |                |
| November 2020          | improvement: Updated UI for managing Roles in ALM.|
|                        | improvement: Account rejection explanation appears on the Request details page.|
|                        | improvement: Requestors can specify a reason for requesting an account renewal.|
|                        | fix: The configuration tab on a Managed Account now updates and reloads automatically after updating a SecretID.|
|                        |                                                    |
| October 2020           |First general availability release of ALM Self-Hosted. 
|                        |
| September 2020         |feature: ServiceNow Requests - ALM’s ServiceNow integration will now support submitting ALM Requests via ServiceNow. This update presents the opportunity for users of ALM and ServiceNow to handle both the Requests and Approval process directly within ServiceNow. Requests can be made for Active Directory and AzureAD accounts.  Note: Customers that already have the ALM ServiceNow application installed in ServiceNow must update to latest version. |                                                                                                                                                            | 
|                        |feature: AzureAD Group Synchronization - ALM now has the ability select AzureAD Groups from a connected Azure Domain and have them synchronized with ALM. This allows the users to leverage existing AzureAD accounts for establishing the userbase for ALM. Any changes made in AzureAD for Groups enabled in the synchronization will automatically updated in ALM, upon the completion of the determined synchronization schedule.   |                                                                                                                                                            |
|                        |                                                                                                                                                                     |                                  
|August 2020             |feature: Inbox - Provides in-app notifications within ALM. Inbox is comprised of three categories of notifications which allows a user to see notifications relevant to their Role and Accounts within ALM.  |
|                        |feature: ALM Engine Local Account Support -  Support for the ALM Engine to allow for a local machine account to run the service. |
|                        |feature: Orphaned Accounts - Set of controls to prevent accounts going without at least one active User or Group assigned as Account Owner. | 
|                        |
|July 2020               |feature: Managed Account Dependencies - Ability for ALM to display the dependencies associated with managed accounts. This is pulled from the Secret Server secret into ALM during the Vault sync. |
|                        |feature: Vault Sync - : Sync functionality updated to allow ad-hoc sync of the vault, as well as enable dependency synchronization. |
|                        |improvement: Tool tips and assisting text added to UI to support aspects of gMSA Workflow Template configuration in ALM. |
|                        |improvement: Dashboard page updated to provide more room for widgets. |
|                        |                                                                                                                                                                     |
|June 2020               |feature: Group Managed Service Accounts (gMSA) Support - A group Managed Service Account (gMSA) provides the same functionality within the domain but also extends that functionality over multiple servers. ALM adds support in the form of the ability to control the lifecycle of gMSA’s.|
|                        |improvement: Reason Column on Approvals Table - Approvers are provided the account request reason directly in the Approvals table, for easier access and expedited review. |
|                        |improvement: Renewal Status in Managed detail screen - To make it easier for Account Owners to view renewal request status, a link has been added in the Account Status row for the ability to navigate from the Managed Account detail page to the request for further detail.|
|                        |                                                                                                                                                                     |
|May 2020                | beta feature: ServiceNow Integration - Ability to reject an ALM Request in ServiceNow. Note: New version of ServiceNow ALM app must be installed.                                                                             |
|                        | improvement: Added the ability to select rows to be displayed in any table in ALM.                                                                                  |
|                        |                                                                                                                                                                     |
|April 2020              | beta feature: ServiceNow Integration - Provides a integration to from ALM, to ServiceNow, for reviewing and approving requests made in ALM.
|                        | feature: EOL OU Retirement - For the use case of keeping Organization Units (OUs) organized and manageable, this feature offers the option to select which OU an account is sent to when ALM disables the account at the end of its determined lifecycle.|
|                        | improvement: Webhook History - A tab in UI of the Webhooks pages allows Administrators and Users with the necessary permissions to view the activity history of a given webhook.|
|                        |                                                                                                                                                                     |
|March 2020              | feature: Azure Active Directory Support - ALM will extend its directory service support to include Azure AD. This will allow ALM to manage accounts located in Azure AD|
|                        | feature: Onboarding Assistance - Users that are synced into ALM from Active Directory will receive an automated email to assist with onboarding the user to ALM.|
|                        |                                                                                                                                                                     |                             
|February 2020           | improvement: Left navigation menu styling update.
|                        | improvement: Update to the design and layout of the Group detail pages. 
|                        | fix: ALM Engine UI configurator tool now launches after the ALM Engine installer finishes. 
|                        |                                                                                                                                                                     | 
|January 2020            | feature: ALM Engine Configuration, will launch a local webpage upon completion of the ALM Engine installer. The tool will assist with testing the setup.             |
|                        | improvement: General application performance enhancements. Enhancements to the Audit log load time.                                                                  |
|                        | improvement: Update to the Managed Account feature which allows a permission set to allow Users with an assigned Custom Role to see all Managed Accounts in ALM.     |
|                        |                                                                                                                                                                     |      
|December 2019           | improvement: increased Secret Server support with DSV now a vault option for managed accounts                                                                       |                                                                                                         |
|                        | improvement: syncing features improved via consolidation of formerly separate syncs to run as a single operation                                                    |
|                        | improvement: new tool allows selection of a specific AD Group for its AD Accounts to be imported and then synced on a schedule                                      |
|                        | improvement: new built-in ALM Group “Everyone” includes all ALM Users; applies new built-in Role of “Account Owner” to let users see their assigned accounts        |
|                        | improvement: the Remote Worker renamed ALM Engine for clarity; beta features previewed in November continue to be available in December as they mature              |
|                        | improvement: new UI detailing on Left Panel Wizards and certain detail pages creates more context and helps customers navigate                                      |
|                        |                                                                                                                                                                     |
| November 2019          | improvement: the Active Directory Account Discovery tool now supports New Account Notification to help ensure all AD accounts benefit from ALM governance tools     |
|                        | improvement: new ALM Engine Calibration feature automates the determination of what ALM Engines have access to what Vaults and AD farms                             |
|                        | improvement: tabbed interface for Vault Details page brings improved usability                                                                                      |
|                        | a beta tool: a new tool for ALM Engine Configuration, intended to streamline the processes related to setting up ALM Engines, is accessible in this update          |
|                        |                                                                                                                                                                     |
| October 2019           | improvement: new Active Directory Account Discovery tool supports bringing any or all service accounts under the management of ALM                                  |
|                        | improvement: System Administrators can select the frequency at which domains automatically sync with ALM, plus commit on-demand sync                                |
|                        | improvement: Workflow Templates let System Administrators define account name prefixes to conform accounts provisioned by ALM to naming conventions                 |
|                        | improvement: better audit logging performance will help organizations with high audit log volumes                                                                   |
|                        | improvement: enhanced external AD sync performance will benefit organizations with larger AD installations                                                          |
|                        | improvement: improved table designs: new row hover highlighting, more obvious labeling when column sorting is available, and stationary header row during scrolling |
|                        | improvement: the design of ALM modules appears more uniform across the application                                                                                  |
|                        | improvement: icons used within ALM feature more effective designs                                                                                                   |
|                        | improvement: the Workflow Template Wizard has an improved visual design                                                                                             |
|                        |                                                                                                                                                                     |
| August 2019            | first General Availability release                                                                                                                                  |
