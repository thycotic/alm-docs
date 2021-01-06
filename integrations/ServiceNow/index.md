[title]: # (Integrate with ServiceNow)
[tags]: # (Account Lifecycle Manager,ALM,ServiceNow)
[priority]: # (5195)

# ServiceNow Integration

ServiceNow delivers popular IT service management solutions. Organizations that employ both Account Lifecycle Manager and ServiceNow IT Service Management can benefit from an integrated workflow. 

As much of other IT management operations are handled in ServiceNow by organizations, now too can the ALM Workflow! This includes the ability in ServiceNow to:
* Submit a Request using an ALM Workflow Templates
* View Request statuses
* View and Approve/Deny Requests for assigned Approvers


## Download the Thycotic ALM ServiceNow App:

1. Log into the ServiceNow Developer Share portal by browsing to https://developer.servicenow.com/connect.do#!/share, and then sign in.
1.  In the “Search Share Projects” field, enter “Thycotic”. Thycotic Account Lifecycle Manager should appear in the results. Click the name to view details.

    ![SN Step 1](images/SN1.png "Service Now Step 1")

1. Click the Download button. This should start the download of the app, in the form of an XML file.

    ![SN Step 2](images/SN2.png "Service Now Step 2")

## Install the Thycotic ALM ServiceNow App:

1. Log in to your instance as a user with the admin role.
1.  In the navigation menu, go to **System Update Sets** > **Retrieved Update Set**.

    ![SN Step 3](images/SN3.png "Service Now Step 3")

1. Click Import Update Set from XML under the Related Links section.

    ![SN Step 4](images/SN4.png "Service Now Step 4")

1. Click Browse..

    * Find and Open the XML file that was previously downloaded.

    * Click Upload.

      ![SN Step 5](images/SN5.png "Service Now Step 5")

    * Thycotic Account Lifecycle Manager should now appear in the list of Retrieved Update Sets records.

1. Click Thycotic Account Lifecycle Manager under the Name column to open up the record.

    ![SN Step 6](images/SN6.png "Service Now Step 6")

1.  Click **Preview Update Set**. An Update Set Preview dialog will appears. Click Close when it is finished.

    ![SN Step 7](images/SN7.png "Service Now Step 7")
    ![SN Step 8](images/SN8.png "Service Now Step 8")

1. Click **Commit Update Set**. An Update Set Commit dialog will appear. Click Close when it is finished.
    
    ![SN Step 9](images/SN9.png "Service Now Step 9")
    ![SN Step 10](images/SN10.png "Service Now Step 10")

1. **Done!** The app should now be installed in the ServiceNow instance. 
    * Reload ServiceNow in your browser.
    * Thycotic Account Lifecycle Manager should now be available in the navigation menu.
    
    ![SN Step 11](images/SN11.png "Service Now Step 11")

## Thycotic ALM ServiceNow App Roles:

In order to access the Thycotic ALM app within ServiceNow, a user must have the admin role or be assigned one of the following roles:

| Role Name           | Role Description |
|---------------------|-------------------------------|
| alm_admin (x_450483_alm_poc.alm_admin)| Provides a user with the ability to create and modify the Configuration for ALM. The Configuration determines which ALM instance ServiceNow will connect to and which credentials are used.|
| alm_approver (x_450483_alm_poc.alm_approver)| Provides a user with the ability to view and approve any ALM request that requires ServiceNow approval.|

## Thycotic ALM ServiceNow App Configuration

1. Sign into your ALM instance as a user with the System Administrator role.
1.  Navigate to **Integrations** > **ServiceNow**

    ![SN Step 12](images/SN12.png "Service Now Step 12")

1. Click **Enable**.
1.  Copy the **Client ID** and **Client Secret** that are provided.
   
    ![SN Step 13](images/SN13.png "Service Now Step 13")

1. Sign into your ServiceNow instance as user with the alm_admin role.
1.  Navigate to **Thycotic Account Lifecycle Manager > ALM Configuration**.
1.  Click the **New** button.

    ![SN Step 14](images/SN14.png "Service Now Step 14")

1. In the new ALM Configuration record, provide:
    * **URL** for your ALM instance
    * **API Client Id** and **API Client Secret** that were given in previous steps
    * Click the **Connect** button.

    ![SN Step 15](images/SN15.png "Service Now Step 15")

1. A message should appear indicating that the “Connection succeeded”. If you receive an error, please double-check the values that were entered.

    ![SN Step 16](images/SN16.png "Service Now Step 16")

1. **Done!** Once the connection has been set up successfully, ServiceNow will be ready to receive requests from ALM.
