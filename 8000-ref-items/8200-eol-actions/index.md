[title]: # (End of Lifecycle Actions Guide)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (8200)

# End of Lifecycle Actions Guide

Account Lifecycle Manager allows the System Administrator to define in the Workflow Template what will happen to an account at the end of its lifecycle.

All accounts provisioned against the Workflow Template will have review actions available in accordance with the determined End of Lifecycle Action. The Requestor will be displayed the End of Lifecycle Action for the Workflow Template they have chosen to provision the account against, as well as be displayed the End of Lifecycle Action on the Managed page.

The End of Lifecycle Action is determined in the Workflow Template will send notifications to the Account Owners indicating attention and action to the account is needed. The date to which the initial notification is sent to Account Owner(s) is also determined by the System Administrator in the Workflow Template. Reminders are sent to the Account Owner(s) periodically on a Workflow Template determined interval before the end of lifecycle. Urgent notifications can be configured in the Workflow Template to remind the Account Owner(s) more frequently leading up to the end of the account’s lifecycle, with an option to include the System Administrator in these notifications.

## End of Lifecycle Actions

* Review

* Disable

* Expire

* Delete

### Review

An account provisioned to an End of  action of Review will in not be turned off in any way when the End of  date is met or exceeded. The intention of Review is to provide a record that the user acknowledges that the account is still required.

Accounts that are have Review as the End of Lifecycle Action will allow the Account Owner three Actions.

* Renew

  This Action button will be enabled on the Managed screen for the account when the date of renewal date is met according to the configuration of the Workflow Template, any date prior the Renew button will be disabled. Selecting Renew will extend the account’s lifecycle until the next Review, based on the account’s chosen Review Interval. Once an account is renewed the Renew button will return to a disabled state until the next review date is met.

* Disable

  This Action button is enabled on the Managed screen for the account at any time of the account’s lifecycle. Selecting Disable will disable the account in Account Lifecycle Manager and Active Directory. After an account is disable the Disable button will pivot to Enable, allowing the user to re-enable the account as needed.

* Delete Account and Secret

  This Action button is enabled on the Managed screen for the account at any time of the account’s lifecycle. Selecting Delete Account and Secret will delete the account and any associated secrets. The user is expected to confirm or cancel this action.

### Disable

An account provisioned to an End of  action of Disable will be disabled in Active Directory at the End of , unless the Account Owner Renews the account prior to the End of .

Accounts that are have Disable as the End of Lifecycle Action will allow the Account Owner three Actions.

* Renew

  This Action button will be enabled on the Managed screen for the account when the date of renewal date is met according to the configuration of the Workflow Template, any date prior the Renew button will be disabled. Selecting Renew will extend the account’s lifecycle until the next Review, based on the account’s chosen Review Interval. Once an account is renewed the Renew button will return to a disabled state until the next review date is met.

* Disable

  This Action button is enabled on the Managed screen for the account at any time of the account’s lifecycle. Selecting Disable will disable the account in Account Lifecycle Manager and Active Directory. After an account is disable the Disable button will pivot to Enable, allowing the user to re-enable the account as needed.

* Delete Account and Secret

  This Action button is enabled on the Managed screen for the account at any time of the account’s lifecycle. Selecting Delete Account and Secret will delete the account and any associated secrets. The user is expected to confirm or cancel this action.

### Expire

An account provisioned to an End of  action of Expire will set the expiration date in Active Directory so that Active Directory will turn the account off at that End of  date, unless the Account Owner submits a request to initiate a new approval to the account prior to the End of  and the Approval process successfully completes with approvals.

Accounts that are have Expire as the End of Lifecycle Action will allow the Account Owner three Actions.

* Start Approvals

  This Action button will be enabled on the Managed screen for the account when the date of renewal date is met according to the configuration of the Workflow Template, any date prior the Start Approvals button will be disabled. Accounts with the End of Lifecycle Action of Expire are required to undergo the Approval Steps again determined by the Workflow Template before the account can be renewed.

  When the ‘Start Approvals’ button is selected by user the Approval Steps will be initiated and the button will pivot to ‘Approvals in Process’ until complete. If Approval is denied by Approval Steps the ‘Start Approvals’ button will be re-enabled to the Account Owner. If the Approval is approved by the Approval Steps the button will be disabled until the next renewal is available for the account.

  Note: The System Administrator that configures a Workflow Template to have Expire as the End of Lifecycle Action should factor in an appropriate time period for when the account is available for renewal by the Account Owner(s) to allow the Approval process to complete prior to expiration. This time period is selected on the Workflow Template for sending initial notifications, which also determines the date the renewal is available.

* Disable

  This Action button is enabled on the Managed screen for the account at any time of the account’s lifecycle. Selecting Disable will disable the account in Account Lifecycle Manager and Active Directory. After an account is disable the Disable button will pivot to Enable, allowing the user to re-enable the account as needed.

* Delete Account and Secret

  This Action button is enabled on the Managed screen for the account at any time of the account’s lifecycle. Selecting Delete Account and Secret will delete the account and any associated secrets. The user is expected to confirm or cancel this action.

### Delete

An account provisioned to an End of  action of Delete will be disabled at the End of , unless the Account Owner Renews the account prior to the End of .

Accounts that are have Expire as the End of Lifecycle Action will allow the Account Owner four Actions.

* Renew

  This Action button will be enabled on the Managed screen for the account when the date of renewal date is met according to the configuration of the Workflow Template, any date prior the Renew button will be disabled. Selecting Renew will extend the account’s lifecycle until the next Review, based on the account’s chosen Review Interval. Once an account is renewed the Renew button will return to a disabled state until the next review date is met.

* Disable

  This Action button is enabled on the Managed screen for the account at any time of the account’s lifecycle. Selecting Disable will disable the account in Account Lifecycle Manager and Active Directory. After an account is disable the Disable button will pivot to Enable, allowing the user to re-enable the account as needed.

* Delete Account and Secret

  This Action button is enabled on the Managed screen for the account at any time of the account’s lifecycle. Selecting Delete Account and Secret will delete the account and any associated secrets. The user is expected to confirm or cancel this action.

* Submit for Approval to Reinstate

  For an account that had an End of Lifecycle Action of 'Delete' and the account wasn't renewed, the account owner may want to 'reinstate' the account. This Review Actions will provide an option to ‘Submit for Approval to Reinstate’.

  When the ‘Submit for Approval to Reinstate’ button is selected by user the Approval Steps will be initiated and the button will pivot to ‘Approvals in Process’ until complete. If Approval is denied by Approval Steps the ‘Submit for Approval to Reinstate’ button will be re-enabled to the Account Owner. If the Approval is approved by the Approval Steps the button will be disabled until the next renewal is available for the account.


