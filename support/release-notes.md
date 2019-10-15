[title]: # (Release Notes)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (8510)

# Release Notes

As a cloud application, ALM lacks version numbers, because updates become available to all users as they occur—the current version is always the only version available. Nonetheless, Thycotic expects to periodically update Account Lifecycle Manager, such as to introduce additional features and provide fixes and improvements.

This article tracks those changes to ALM. Highlights of the most recent update appear first. The same information appears in abbreviated form in the table that follows, forming a change log.

## October 2019 Release Notes Highlights

October saw Account Lifecycle Manager add new features, improve performance, and refine its design for improved usability.

### Active Directory Account Discovery

Using ALM’s Active Directory Account Discovery tool, System Administrators can select service accounts in their Active Directory Domains and import them into ALM. The tool follows a simple process to select the desired service accounts, assign accounts to ALM Workflows, and assign ownership. This major new tool allows the customer to bring any or all service accounts under the management of Account Lifecycle Manager.

### Domain Synchronization Scheduling

System Administrators can select the frequency at which domains automatically sync with Account Lifecycle Manager. Additionally, they can commit an on-demand sync. This allows synchronization of Users, Groups, Attributes, and Organizational Units.

### Account Name Prefixes

System Administrators can define an account name prefix when they build a Workflow Template, so that any accounts created pursuant to selection of the Workflow Template by account requesters will be named to include the designated prefix. This allows accounts provisioned by ALM to conform to naming conventions for organizational purposes.

### Performance Enhancements

Performance enhancements apply to the Audit Log and AD External Group Sync:

* **Audit Log**: Organizations with large volumes of audit log entries will benefit from audit log performance enhancements.
* **AD External Group Sync**: Organizations with larger AD installations will notice the improved performance of the external group sync function.

### UI/UX Enhancements

Enhancements to the user interface and design language of ALM this October include:

* The table design includes productivity enhancements.
  * A visual hover state now applies to rows.
  * Columns include an improved chevron design to make it more apparent when you can sort by the contents of a column.
  * The header row remains visible as you scroll through longer tables.
* The design of ALM modules appears more uniform across the application.
* Icons used within ALM have an improved design.
* The Workflow Template Wizard has a new appearance.

## Account Lifecycle Manager: Change Log

| **Update**             | **Notes**                                  |
|------------------------|--------------------------------------------|
| October 2019           | improvement: new Active Directory Account Discovery tool supports bringing any or all service accounts under the management of ALM |
|                        | improvement: System Administrators can select the frequency at which domains automatically sync with ALM, plus commit on-demand sync |
|                        | improvement: Workflow Templates let System Administrators define account name prefixes to conform accounts provisioned by ALM to naming conventions |
|                        | improvement: better audit logging performance will help organizations with high audit log volumes |
|                        | improvement: enhanced external AD sync performance will benefit organizations with larger AD installations |
|                        | improvement: improved table designs: new row hover highlighting, more obvious labeling when column sorting is available, and stationary header row during scrolling |
|                        | improvement: the design of ALM modules appears more uniform across the application |
|                        | improvement: icons used within ALM feature more effective designs |
|                        | improvement: the Workflow Template Wizard has an improved visual design |
|                        |      |
| August 2019            | first General Availability release  |

