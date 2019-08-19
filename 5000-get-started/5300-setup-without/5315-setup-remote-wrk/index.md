[title]: # (Setup the Remote Worker Service)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (5315)

### Setup the Remote Worker Service

The Remote Worker is a Windows Service that runs on your organization’s hardware. It manages interactions between the ALM cloud service and your Active Directory installation. It also supports ALM’s integration with your organization’s Secret Server instance.

#### Remote Worker Installation

To install a new Remote Worker, go to the **Remote Worker Pools** section of ALM. Use **Download Installer** to obtain the installer files.

Copy the installer to the computer that will host the Remote Worker. Unzip the file and run:

  `setup_x86.cmd`

Follow the prompts until the installation finishes.

#### Remote Worker Logon Account Configuration in AD

Change the logon account for the Thycotic Remote Worker to an AD account with the following AD permissions.

**Minimum Remote Worker AD Service Account Permissions**

  
---
  

**Minimum Remote Worker AD Service Account Permissions**

| AD Object           | Permissions for Remote Worker |
|---------------------|-------------------------------|
| organizational unit | list contents                 |
|                     | read all properties           |
|                     | create user objects           |
|                     | delete user objects           |
| user                | list contents                 |
|                     | read all properties           |
|                     | change password               |
|                     | reset password                |
|                     | write all properties          |
| groups              | list contents                 |
|                     | read all properties           |
|                     | write member                  |

  
---
  
To change the logon account:

* Run **services.msc** to open the **Services Control Manager**.

* Find **Thycotic Remote Worker**, right-click, and select **Properties**.

* In the Properties panel, select **Log On**.

* Select **This account:**

* Supply the AD account name for the Remote Worker service.

* Supply the account credentials.

* Click **OK**.

* Restart the Remote Worker service by right clicking **Thycotic Remote Worker** and selecting **Restart**.

* In ALM, the new Remote Worker appears in the **Unassigned Remote Workers** section.

* Click the Remote Worker, assign it to a pool, and click **Activate**.

#### Additional Remote Worker Logon Account Information

The Remote Worker’s AD Service Account requires several machine-specific permissions. The installer sets these permissions, but you may need to reapply them if the service account changes.

* Local Security or Domain Policy: “Log on as a service”

* Registry: Full Control on `Computer\\HKLM\\SOFTWARE\\Thycotic Software Ltd`

* File System: `C:\\ProgramData\\Thycotic Software Ltd`

#### Remote Worker Logs

Admins can view Remote Worker error messages and sync information in the Remote Worker Log, available in ALM under **Audit > Remote Worker Logs**. This is an abbreviated log; the Remote Worker does not send all log messages back to ALM.

You can view the full logs in these locations on the machine hosting the Remote Worker service:

* C:\\ProgramData\\Thycotic Software Ltd\\RemoteWorker\\logs

* C:\\ProgramData\\Thycotic Software Ltd\\RemoteWorker\\packages\\Thycotic Provisioning\\logs

To change the log level, update the `appsettings.json` file and restart the Remote Worker service.

* C:\\ProgramData\\Thycotic Software Ltd\\RemoteWorker\\packages\\Thycotic Provisioning\\appsettings.json

### LDAPS

ALM requires LDAPS for AD integration, with reliance on port 636; the port number is not configurable.

### Remote Worker: Troubleshooting

If the Remote Worker does not run properly, review its operation logs for clues.

If you cannot resolve the problem, contact Thycotic for support.

