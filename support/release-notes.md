[title]: # (Release Notes)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (8510)

# Release Notes

As a cloud application, ALM lacks version numbers, because updates become available to all Users as they occur—the current version is always the only version available. Nonetheless, Thycotic expects to periodically update Account Lifecycle Manager, such as to introduce additional features and provide fixes and improvements.

This article tracks those changes to ALM. Highlights of the most recent update appear first. The same information appears in abbreviated form in the table that follows, forming a change log.

## November 2019 Release Notes Highlights

November saw Account Lifecycle Manager add New Account Notifications (an Account Discovery feature), Remote Worker Calibration (a Vault tool), and more usable Vault Detail pages, which now sport a tabbed interface. You can also opt to try out the beta release of a tool that will streamline the processes for setting up Remote Workers.

### New Account Notifications

October saw the addition of the Active Directory Account Discovery Tool, which provided bulk discovery and import of extant AD accounts when introducing ALM to the enterprise or extending its reach. With this November’s update, you can catch new accounts as they appear—when ALM discovers new accounts in AD that have been created with no corresponding managed account record in ALM, it sends an email naming the AD accounts to the System Administrator.

ALM includes a Webhook for this event notification, allowing you to set up additional events to occur automatically when ALM finds unmanaged accounts in AD.

### Remote Worker Calibration

ALM can automatically assess which Remote Workers can connect to what Secrets vaults and directory services. MSPs may particularly embrace this tool, as they often must deal with multiple Secrets vaults and AD environments.

### Tabbed Interface for Vault Detail Pages

The tabbed interface now applied to Vault Detail pages increases the volume of information available for ready perusal, while making the User interface less cluttered.

### Beta Feature Release: Remote Worker Configuration Website Tool

On successful installation of a Remote Worker on a machine, a website hosted locally on that machine will be set to automatically load to provide an interface and toolset for configuring the Secret Server vault, setting up the External Domain (Active Directory), and creating Remote Worker Pools. This should streamline the overall setup process for Remote Workers.

In this November beta release of the feature it has been set not to autoload. To learn how you can try out this beta feature, see [Setup the Remote Worker Service](../get-started/setup-remote-wrk/).

## Account Lifecycle Manager: Change Log

| **Update**             | **Notes**                                                                                                                                                           |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| November 2019          | improvement: the Active Directory Account Discovery tool now supports New Account Notification to help ensure all AD accounts benefit from ALM governance tools     |
|                        | improvement: new Remote Worker Calibration feature automates the determination of what Remote Workers have access to what Vaults and AD farms                       |
|                        | improvement: tabbed interface for Vault Details page brings improved usability                                                                                      |
|                        | a beta tool: a new tool for Remote Worker Configuration, intended to streamline the processes related to setting up Remote Workers, is accessible in this update    |
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
