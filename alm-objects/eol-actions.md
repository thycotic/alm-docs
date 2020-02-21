[title]: # (At End of Lifecycle Actions)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,End of Lifecycle Actions, AEOL,)
[priority]: # (2300)

# At End of Lifecycle (AEOL) Actions

Account Lifecycle Manager allows a System Administrator to define in a Workflow Template the At End of Lifecycle actions (AEOLs) that will apply to accounts provisioned against that Workflow Template. The Template also controls the schedule and pacing of Notifications to be sent by ALM as the End of Lifecycle date approaches, and the parties who will receive the Notifications.

When an account comes up for review at or near the end of its lifecycle, ALM sends Notifications to the Users or Groups designated in the Workflow Template and as scheduled in that Template.

The actions ALM allows reviewers to take correspond to the At End of Lifecycle actions specified by the Workflow Template. These may include:

* Review
* Disable
* Expire
* Delete

## Review

An account provisioned with an AEOL action of Review will not be curtailed in any way with passage of the End of Lifecycle date. The Review action serves simply to document a User’s acknowledgement that the account remains necessary.

Reviewers of an account that has Review as the AEOL action have three choices:

* Renew

  Before the Renewal Date set in the applicable Workflow Template, the **Renew** option is unavailable. Beginning on the Renewal Date, the Renew option is available.

  Selecting Renew extends the account’s lifecycle until the next Review, based on the Review Interval set in the Workflow Template. The renewal period will start at UTC 00:00. On renewal of the Account, the Renew option will become unavailable until the next review date.

* Disable

  The **Disable** option will disable the account in ALM **and** in Active Directory. Once selected, this option is replaced by a choice to **Enable**, allowing the User to re-enable the account as needed.

* Delete Account and Secret

  The **Delete Account and Secret** option will delete the account and any associated secrets. Selecting this option requires the User to confirm (or cancel) the action.

## Disable

An account provisioned with an AEOL action of **Disable** will be disabled in Active Directory at the End of Lifecycle, unless the Account Owner Renews the account prior to the End of Lifecycle date.

Reviewers of an account that has Disable as the AEOL action have three choices:

* Renew

  Before the Renewal Date set in the applicable Workflow Template, the **Renew** option is unavailable. Beginning on the Renewal Date, the Renew options is available.

  Selecting Renew will extend the account’s lifecycle until the next Review, based on the Review Interval set in the Workflow Template.The renewal period will start at UTC 00:00. On renewal of the account, the Renew option will again be unavailable until the next Review Date.

* Disable

  The **Disable** option will disable the account in ALM **and** in Active Directory. Once selected, this option is replaced by a choice to **Enable**, allowing the User to re-enable the account as needed.

* Delete Account and Secret

 The **Delete Account and Secret** option will delete the account and any associated secrets. Selecting this option requires the User to confirm (or cancel) the action.

## Expire

For an account provisioned with an AEOL action of **Expire**, ALM sets the Expiration Date in Active Directory such that AD will disable the account at the End of Lifecycle date unless the Account Owner renews the account prior to that date.

Accordingly, the first option likely to become available to the Account Owner who will review the Account is the option to **Submit for Approval to Renew**, offered by a Notification sometime in advance of the End of Lifecycle date so that the Account can be renewed before it would otherwise expire.

* A System Administrator who configures a Workflow Template with Expire as the End of Lifecycle Action must decide how far in advance of the End of Lifecycle date to set the Renewal Date, bearing in mind that the Approval to Renew process duplicates the entire original approval process.
* The Renewal Date set by the Administrator controls the timing of initial Notifications to the Account Owner.

Account Owners reviewing an account that has Expire as the AEOL action have three choices:

* Submit for Approval to Renew

  Before the Renewal Date set in the applicable Workflow Template, this choice will not be available. Beginning on the Renewal Date, this action is available to the Account Owner.

  Choosing to renew initiates the Approval Steps specified in the associated Workflow Template and replaces the selection to *Submit for Approval to Renew* with an *Approvals in Process* notation.

  * If Approval is denied, the notation switches back to Submit for Approval to Renew and remains that way until and after the Account expires.
  * If the Approval is granted, the *Approvals in Process* notation is removed, and the account is renewed for the renewal period defined at UTC 00:00. The Submit for Approval to Renew option remains unavailable until the next Renewal Date.

* Disable

  The **Disable** option will disable the account in ALM **and** in Active Directory. Once selected, this option is replaced by a choice to **Enable**, allowing the User to re-enable the account as needed.

* Delete Account and Secret

  The **Delete Account and Secret** option will delete the account and any associated secrets. Selecting this option requires the User to confirm (or cancel) the action.

## Delete

An account provisioned with an AEOL action of **Delete** will be disabled (not actually deleted) at the End of Lifecycle date, unless the Account Owner renews the account prior to that date.

Reviewers of an account that has Delete as the AEOL action have three (sometimes four) choices:

* Disable

  The **Disable** option will disable the account in ALM **and** in Active Directory. Once selected, this option is replaced by a choice to **Enable**, allowing the User to re-enable the account as needed.

* Delete Account and Secret

  The **Delete Account and Secret** option will delete the account and any associated secrets. Selecting this option requires the User to confirm (or cancel) the action.

* Submit for Approval to Reinstate

  If an account owner does not renew an account that has an AEOL action of Delete, ALM disables the account, and the End of Lifecycle Review options update to include the **Submit for Approval to Reinstate** option.

  On selection of this option, the original Approval Process begins anew, and the Submit for Approval to Reinstate option gives way to an **Approvals in Process** notation.

  * If Approval is denied, the notation switches back to **Submit for Approval to Reinstate**.

  * If the Approval is granted, the notation is removed, and the Submit for Approval to Reinstate option becomes unavailable until the next Renewal Date. The renewal period will start at UTC 00:00 following Approval.
  
  See the [End-of-Lifecycle Account Disposition Logic](eol-actions-logic.md) article for details on the logic of options availability vs. account status and review actions.
  