[title]: # (Install a Remote Worker)
[tags]: # (,)
[priority]: # (1510)
## Install a Remote Worker

To setup a new remote worker, first go to the Remote Worker Pools section. Then click Download Installer.

![](images/placeholder.gif)

You will then be prompted to download a zip file. Save the file and copy to the computer that will host the Remote Worker.

Unzip the file and run setup_x86.cmd.

![](images/placeholder.gif)v

Follow the remaining prompts until the installation is finished.

Once complete, the Log On account for the Thycotic Remote Worker must be changed to an AD account with the following AD permissions:

* Create, delete, and manage user accounts
* Reset user passwords and force password change at next logon
* Read all user information
* Modify the membership of a group

To change the Log On account, open the Services Control Manager by running *services.msc.* Find Thycotic Remote Worker, right-click and select Properties.

![](images/placeholder.gif)

In the Properties dialog, select Log On. Then select “This account:”. Provide the AD account name for the Remote Worker service, the account credentials, then click OK.

![](images/placeholder.gif)

Restart the service by right-clicking “Thycotic Remote Worker” and selecting Restart.

![](images/placeholder.gif)

After the Remote Worker is up and running, it must be activated and assigned to a Remote Worker Pool. The new Remote Worker should now appear in the Unassigned Remote Workers section.

![](images/placeholder.gif)

Click the Remote Worker, assign it to a pool, then click Activate.

![](images/placeholder.gif)