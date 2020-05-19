[title]: # (Release Notes)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (8450)

# Release Notes

As a cloud application updates become available to all Users as they occur—the current version is always the only version available. Thycotic periodically updates Account Lifecycle Manager to introduce additional features and provide fixes and improvements.

This article tracks those changes to ALM.

## Account Lifecycle Manager: Change Log

| **Update**             | **Notes**                                                                                                                                                           |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
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
