[title]: # (Build Workflow Templates)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (6000)

# Calibrating the ALM Engine

To use the ALM Engine Calibration tool:

1. Go to the **Vaults** page.
2. Select the Vault for which you need an active ALM Engine connection to be established.
3. On the **Vault Details** page, go to the **ALM Engines** tab.
4. Click **Calibration**.

This will queue a **ALM Engine Calibration Job** and prompt a modal dialog stating:

* ALM Engine Calibration started, this may take several minutes to complete.

The ALM Engine Calibration Job connects with the ALM Engines, tasking each one to authenticate with the Secret Server Vault you selected. The Calibration Job keeps track of which ALM Engines successfully authenticate to the Vault, creating a list of ALM Engines known to have access to that Secret Server.

* That list populates a table on the ALM Engines tab of the Vault Details page.
* ALM Engines that did not authenticate will not appear on the list.
* If no ALM Engine authenticated, the Vault Details page will indicate that “No ALM Engines calibrated to integration.”

An ALM Engines Calibration Job runs as part of any Scheduled Sync for a Vault, with the list of successfully authenticating ALM Engines updating on completion of the sync job.