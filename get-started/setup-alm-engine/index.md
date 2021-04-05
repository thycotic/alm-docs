[title]: # (Setup the ALM Engine Service)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5120)

# Setup the ALM Engine Service

The ALM Engine is a Windows Service that runs on your organization’s hardware. It manages interactions between the ALM cloud service and your Active Directory installation. It also supports ALM’s integration with your organization’s Secret Server instance.

## ALM Engine Service Requirements

The ALM Engine Windows service must:

* be able to reach your domain controller over LDAPS
* run on a domain controller or domain-joined machine, with
  * Windows Server 2012 or later, and
  * Microsoft .NET 4.7.1 or later installed
* run as a non-domain joined computers automatically using Network Service as the service account, *OR* as an AD account with AD permissions to:
  * create, delete, and manage User accounts
  * reset User passwords and force next-logon password changes
  * read all User information
  * modify the membership of a Group

### Required Ports

The ALM Engine will communicate to *.accountlifecyclecloud.com over port 443

> Note: ALM Engine will communicate through port 5671 to the below Urls for each region

| Region | URL| Port|
|---|---|---|
| **US East**| thycotic-enza-prod-eastus-sb01.servicebus.windows.net | 5671|
| **AU Cen**| thycotic-enza-prod-auscen-sb01.servicebus.windows.net |5671|
|**CAN Cen**| thycotic-enza-prod-cac-sb01.servicebus.windows.net |5671|
|**EU West**| thycotic-enza-prod-westeuro-sb01.servicebus.windows.net |5671|

## ALM Engine Installation

To install a new ALM Engine, go to the **ALM Engine** section of ALM. Use **Download Installer** to obtain the installer files.

Copy the installer to the computer that will host the ALM Engine. Unzip the file and run:

  `install.cmd`

Follow the prompts until the installation finishes.

>**NOTE**: The activation token for the ALM Engine will last **8 hours**. If the engine needs to be reinstalled, a new token will need to be obtained.

### ALM Engine Configuration Website Tool

* On successful installation of an ALM Engine on a machine, the ALM Engine Configuration Website Tool (hosted locally on the ALM Engine machine) will automatically load.
  * To manually access the address is: localhost:14568
* The website will provide an interface and toolset for these tasks:
  * configuring the Vault
  * setting up the External Domain (Active Directory)
  * creating ALM Engine Pools

## ALM Engine Logon Account Configuration in AD

Change the logon account for the Thycotic ALM Engine to an AD account with the following AD permissions.

**Table:** *ALM Engine AD Service Account Permissions*

| AD Object           | Permissions for ALM Engine |
|---------------------|-------------------------------|
| Organizational Unit | list contents                 |
|                     | read all properties           |
|                     | create User objects           |
|                     | delete User objects           |
| User                | list contents                 |
|                     | read all properties           |
|                     | change password               |
|                     | reset password                |
|                     | write all properties          |
| Groups              | list contents                 |
|                     | read all properties           |
|                     | write member                  |

---
  
To change the logon account:

1. Run **services.msc** to open the **Services Control Manager**.
1. Find **Thycotic ALM Engine**, right-click, and select **Properties**.
1. In the Properties panel, select **Log On**.
1. Select **This account:**
1. Supply the AD account name for the ALM Engine service and the account credentials. Click **OK**.
1. Restart the ALM Engine service by right clicking **Thycotic ALM Engine** and selecting **Restart**.
1. Back in ALM, the new ALM Engine will appear in the **Unassigned ALM Engines** section.
1. Click the ALM Engine, assign it to a pool, and click **Activate**.

## Additional ALM Engine Logon Account Information

The ALM Engine’s AD Service Account requires several machine-specific permissions. The installer sets these permissions, so you will not need to perform these steps as part of your initial ALM setup. However, take note that if the service account changes, you may need to reapply these permissions:

* Local Security or Domain Policy: “Log on as a service”
* Registry: Full Control on `Computer\HKLM\SOFTWARE\Thycotic Software Ltd`
* File System: `C:\ProgramData\Thycotic Software Ltd`

## ALM Engine Logs

Admins can view ALM Engine error messages and sync information in the **ALM Engine Log**, available in ALM under **Audit > ALM Engine Logs**. This is an abbreviated log; the ALM Engine does not send all log messages back to ALM.

## View Full Versions of ALM Engine Logs

Use these steps to view the full logs on the machine hosting the ALM Engine service:

1. Log into the machine where the ALM Engine is located.
1. From root, navigate to: ProgramData > Thycotic Software Ltd > ALMEngine > packages > Thycotic Provision
1. Locate the `appsettings.json` file.
1. Open `appsettings.json` with Notepad or other suitable text editor.
1. Under the **Serilog** section, you will see **MinimumLevel**, and below that, **Default** : **Information**
1. Change that to **Default** : **Verbose**
1. Save the file.
1. Open **Services**
1. Restart the ALM Engine service.

## LDAPS

ALM requires LDAPS for AD integration, with reliance on port 636; the port number is not configurable.

## ALM Engine: Troubleshooting

If the ALM Engine does not run properly, review its operation logs for clues. If you cannot resolve the problem, [contact Thycotic for support](../../support/).

## See Also

**See Also** the *ALM Engine Calibration Tool* section of the [ALM Administration](../../alm-admin/) article.
