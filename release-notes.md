[title]: # (Release Notes)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (8450)

# Release Notes

As a cloud application, ALM lacks version numbers, because updates become available to all Users as they occur—the current version is always the only version available. Nonetheless, Thycotic expects to periodically update Account Lifecycle Manager, such as to introduce additional features and provide fixes and improvements.

This article tracks those changes to ALM. Highlights of the most recent update appear first. The same information appears in abbreviated form in the table that follows, forming a change log.

## December 2019 Release Highlights

With December’s release, Account Lifecycle Manager gained more robust Active Directory user synchronization, with formerly separate sync operations consolidated to obtain full domain synchronization. Two new built-in objects, the Everyone Group and the Account Owner Role, combine to remove much of the administrative overhead for the bulk of ALM users. Finally, a matured Remote Worker has taken on a new name, ALM Engine, to better indicate its nature, and its recently released beta features continue to mature with the December release.

### Beta Feature Release: ALM Engine Configuration Website Tool

On successful installation of an ALM Engine on a machine, a website hosted locally on that machine will be set to automatically load to provide an interface and toolset for configuring the Secret Server vault, setting up the External Domain (Active Directory), and creating ALM Engine Pools. This should streamline the overall setup process for ALM Engines.

In this December’s second monthly release of the feature in beta, it remains set not to autoload. To learn how you can try out this beta feature, see [Setup the ALM Engine Service](../get-started/setup-alm-engine/).

## Account Lifecycle Manager: Change Log

| **Update**             | **Notes**                                                                                                                                                           |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| December 2019          | improvement: syncing with Active Directory now takes less effort, with sync consolidation more automated and secured                                                |
|                        | a new built-in Everyone Group and Account Owner Role combine to remove much administrative overhead for the bulk of ALM users                                       |
|                        | the Remote Worker tool, now named ALM Enginer, continues to mature, with its advanced configuration tool again available this month in beta                         |
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
