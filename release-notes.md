[title]: # (Release Notes)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (8450)

# Release Notes

As a cloud application, ALM lacks version numbers, because updates become available to all Users as they occur—the current version is always the only version available. Nonetheless, Thycotic expects to periodically update Account Lifecycle Manager, such as to introduce additional features and provide fixes and improvements.

This article tracks those changes to ALM. Highlights of the most recent update appear first. The same information appears in abbreviated form in the table that follows, forming a change log.

## December 2019 Release Highlights

ALM has increased Secret Server support by adding DevOps Secrets Vault as a vault option for managed accounts.

ALM’s Active Directory syncing features improved via consolidation of formerly separate syncs. Syncs that until now had to be run separately for particular types of AD objects now can be run together as a single operation.

A new tool allows you to select a specific AD Group and have its AD Accounts imported and subsequently synced on a schedule.

A new built-in ALM Group, Everyone, automatically includes all ALM Users and applies thereby the new built-in Role of Account Owner, allowing a user to view their owned (assigned) accounts.

The Remote Worker has been renamed ALM Engine to make its function more readily understood, and its beta features previewed in November continue to be available in December as they mature.

New UI detailing on Left Panel Wizards and certain detail pages provide improved context and cognitive cueing about items displayed to (and actions requested of) the user.

## Beta Feature Release: ALM Engine Configuration Website Tool

On successful installation of an ALM Engine on a machine, a website hosted locally on that machine will be set to automatically load to provide an interface and toolset for configuring the Secret Server vault, setting up the External Domain (Active Directory), and creating ALM Engine Pools. This should streamline the overall setup process for ALM Engines.

In this December’s second monthly release of the feature in beta, it remains set not to autoload. To learn how you can try out this beta feature, see [Setup the ALM Engine Service](../get-started/setup-alm-engine/).

## Account Lifecycle Manager: Change Log

| **Update**             | **Notes**                                                                                                                                                           |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| December 2019          | improvement: increased Secret Server support with DSV now a vault option for managed accounts                                                                       |
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
