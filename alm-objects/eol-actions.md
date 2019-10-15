[title]: # (End of Lifecycle Actions)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (2300)

# End of Lifecycle Actions

Account Lifecycle Manager allows a System Administrator to define in a Workflow Template the End of Lifecycle Actions (EOL Actions) that will apply to accounts provisioned against that Workflow Template. The Template also controls the schedule and pacing of Notifications to be sent by ALM as the End of Lifecycle date approaches, and the parties who will receive the Notifications.

When an account comes up for review at or near the end of its lifecycle, ALM sends Notifications to the Users or Groups designated in the Workflow Template, and as scheduled in that Template.

The actions ALM allows reviewers to take correspond to the End of Lifecycle Actions specified by the Workflow Template. These may include:

* Review

* Disable

* Expire

* Delete

### Review

An account provisioned with an EOL Action of Review will not be curtailed in any way with passage of the End of Lifecycle date. The Review action serves simply to document a User’s acknowledgement that the account remains necessary.

Reviewers of an account that has Review as the EOL Action have three choices:

* Renew

  Before the Renewal Date set in the applicable Workflow Template, the Renew button is disabled. Beginning on the Renewal Date, the Renew button is enabled. 

  Selecting Renew extends the account’s lifecycle until the next Review, based on the Review Interval set in the Workflow Template. On renewal of the account, the Renew button will return to a disabled state until the next review date.

* Disable

  The Disable button, always enabled if present, will disable the account in ALM **and** in Active Directory. The button then switches to Enable, allowing the user to re-enable the account as needed.

* Delete Account and Secret

  The Delete Account and Secret button, always enabled if present, will delete the account and any associated secrets. Selecting this option requires the user to confirm (or cancel) the action.

### Disable

An account provisioned with an EOL Action of Disable will be disabled in Active Directory at the End of Lifecycle, unless the Account Owner Renews the account prior to the End of Lifecycle date.

Reviewers of an account that has Disable as the EOL Action have three choices:

* Renew

  Before the Renewal Date set in the applicable Workflow Template, the Renew button is disabled. Beginning on the Renewal Date, the Renew button is enabled. 

  Selecting Renew will extend the account’s lifecycle until the next Review, based on the Review Interval set in the Workflow Template. On renewal of the account, the Renew button will return to a disabled state until the next review date.

* Disable

  The Disable button, always enabled if present, will disable the account in ALM **and** in Active Directory. The button then switches to Enable, allowing the user to re-enable the account as needed.

* Delete Account and Secret

  The Delete Account and Secret button, always enabled if present, will delete the account and any associated secrets. Selecting this option requires the user to confirm (or cancel) the action.

### Expire

For an account provisioned with an EOL Action of Expire, ALM sets the Expiration date in Active Directory so that AD will disable the account at the End of Lifecycle date, unless the Account Owner renews the account prior to that date.

* Renewing an account with the Expire EOL Action requires repetition of the entire original approval process.

* A System Administrator who configures a Workflow Template with Expire as the End of Lifecycle Action must decide how far in advance of the End of Lifecycle date to set the Renewal Date, given the requirement for repetition of the original approval process.

* The Renewal Date controls the timing of initial Notifications to the Account Owner. The Start Approvals button is disabled before the Renewal Date.

Reviewers of an account that has Expire as the EOL Action have three choices:

* Start Approvals

  Before the Renewal Date set in the applicable Workflow Template, the Start Approvals button is disabled. Beginning on the Renewal Date, the Start Approvals button is enabled. 

  Using the Start Approvals button initiates the Approval Steps specified in the associated Workflow Template. The Start Approvals button then relabels as Approvals in Process.

  * If Approval is denied, the button switches back to Start Approvals.

  * If the Approval is granted, the button label switches back to Start Approvals and the button becomes disabled until the next Renewal Date. 

* Disable

  The Disable button, always enabled if present, will disable the account in ALM **and** in Active Directory. The button then switches to Enable, allowing the user to re-enable the account if needed.

* Delete Account and Secret

  The Delete Account and Secret button, always enabled if present, will delete the account and any associated secrets. Selecting this option requires the user to confirm (or cancel) the action.

### Delete

An account provisioned with an EOL Action of Delete will be disabled (not actually deleted) at the End of Lifecycle date, unless the Account Owner renews the account prior to that date.

Reviewers of an account that has Delete as the EOL Action have three (sometimes four) choices:

* Renew

  Before the Renewal Date set in the applicable Workflow Template, the Renew button is disabled. Beginning on the Renewal Date, the Renew button is enabled. 

  Selecting Renew will extend the account’s lifecycle until the next Review, based on the Review Interval set in the Workflow Template. On renewal of the account, the Renew button will return to a disabled state until the next review date.

* Disable

  The Disable button, always enabled if present, will disable the account in ALM **and** in Active Directory. The button then switches to Enable, allowing the user to re-enable the account as needed.

* Delete Account and Secret

  The Delete Account and Secret button, always enabled if present, will delete the account and any associated secrets. Selecting this option requires the user to confirm (or cancel) the action.

* Submit for Approval to Reinstate

  If an account owner does not renew an account that has an EOL Action of Delete, ALM disables the account, and the End of Lifecycle the Review options update to include the Submit for Approval to Reinstate option.

  On selection of this option, the original approval process begins anew, and the Submit for Approval to Reinstate button label switches to Approvals in Process.

  Using the Submit for Approval to Reinstate button initiates the Approval Steps specified in the associated Workflow Template; the button relabels as Approvals in Process.

  * If Approval is denied, the button switches back to Submit for Approval to Reinstate.

  * If the Approval is granted, the button label switches back to Submit for Approval to Reinstate and the button becomes disabled until the next Renewal Date. 


