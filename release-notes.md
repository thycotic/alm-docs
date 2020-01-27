[title]: # (Release Notes)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (8450)

# Release Notes

As a cloud application, ALM lacks version numbers, because updates become available to all Users as they occur—the current version is always the only version available. Nonetheless, Thycotic expects to periodically update Account Lifecycle Manager, such as to introduce additional features and provide fixes and improvements.

This article tracks those changes to ALM. Highlights of the most recent update appear first. The same information appears in abbreviated form in the table that follows, forming a change log.

## January 202 Release Highlights
A new tool, ALM Engine Configuration, will launch a local webpage upon completion of the ALM Engine installer on the machine the ALM Engine was installed upon. The tool will assist with the initial configuration and testing process. 

An update to the Managed Account feature in Roles allows the use case for a User to see all Managed accounts. A User with a Custom Role assigned that has the “Read” and “Manage” permission enabled on the “Managed Account” feature will allow the User to see all Managed Accounts. Previously, the User could only see Managed Accounts to which they are an assigned owner of, without a method to see the full inventory of Managed Service accounts in ALM. 

ALM has increased the performance across the application. Improvements to the Audit logs in the application will improve load times. 

## Account Lifecycle Manager: Change Log

| **Update**             | **Notes**                                                                                                                                                           |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|January 2020            |feature: ALM Engine Configuration, will launch a local webpage upon completion of the ALM Engine installer. The tool will assist with testing the setup.             |
|                        |improvement: General application performance enhancements. Enhancements to the Audit log load time.                                                                  |
|                        |improvement: Update to the Managed Account feature which allows a permission set to allow Users with an assigned Custom Role to see all Managed Accounts in ALM.     |
|                        |                                                                                                                                                                     |      
|December 2019           | improvement: increased Secret Server support with DSV now a vault option for managed accounts                                                                                                                                                                                 |
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
