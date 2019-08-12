[title]: # (Setup the Remote Worker Service)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (5405)

### Setup the Remote Worker Service

The Remote Worker is a Windows Service that runs on your organization’s hardware. It manages interactions between the ALM cloud service and your Active Directory installation. It also supports ALM’s integration with your organization’s Secret Server instance.

#### Remote Worker Installation

To install a new Remote Worker, go to the **Remote Worker Pools** section of ALM. Use **Download Installer** to obtain the installer files.

Copy the installer to the computer that will host the Remote Worker. Unzip the file and run:

setup_x86.cmd

Follow the prompts until the installation finishes.

#### Remote Worker Logon Account Configuration

Next, change the logon account for the Thycotic Remote Worker to an AD account with the following AD permissions:

* create, delete, and manage user accounts

* reset user passwords and force password change at next logon

* read all user information

* modify the membership of a group

To change the logon account:

* Run **services.msc** to open the **Services Control Manager**.

* Find **Thycotic Remote Worker**, right-click, and select **Properties**.

* In the Properties panel, select **Log On**.

* Select **This account:**

* Supply the AD account name for the Remote Worker service.

* Supply the account credentials.

* Click **OK**.

* Restart the service by right clicking **Thycotic Remote Worker** and selecting **Restart**.

* In ALM, the new Remote Worker appears in the **Unassigned Remote Workers** section.

* Click the Remote Worker, assign it to a pool, and click **Activate**.

#### Remote Worker: Troubleshooting

If the Remote Worker does not run properly, review the logs of its operation for clues.

* C:\\ProgramData\\Thycotic Software Ltd\\RemoteWorker\\packages\\Thycotic Provisioning\\logs

* C:\\ProgramData\\Thycotic Software Ltd\\RemoteWorker\\logs

If you cannot resolve the problem, contact Thycotic for support.

