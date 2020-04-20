[title]: # (ServiceNow Integration)
[tags]: # (Account Lifecycle Manager,ALM,ServiceNow)
[priority]: # (5195)

#ServiceNow Integration (Beta)

ServiceNow delivers popular IT service management solutions. Organizations that employ both Account Lifecycle Manager and ServiceNow IT Service Management can benefit from an integrated workflow. 

In the April release of ALM the integration provides a beta version of an integration to ServiceNow to interact with the Request Approval process for ALM accounts. 

As much of other IT management operations are handled in ServiceNow by organizations, now too can service account approval via ALM be handled from the same workflow. 

##Download the Thycotic ALM ServiceNow App:

* Log into the ServiceNow Developer Share portal by browsing to https://developer.servicenow.com/connect.do#!/share, and then sign in.

* In the “Search Share Projects” field, enter “Thycotic”. Thycotic Account Lifecycle Manager should appear in the results. Click the name to view details.

    ![SN Step 1](images/SN1.png)

* Click the Download button. This should start the download of the app, in the form of an XML file.

    ![SN Step 2](images/SN2.png)

##Install the Thycotic ALM ServiceNow App:

* Log in to your instance as a user with the admin role.

* In the navigation menu, go to **System Update Sets** > **Retrieved Update Set**.

    ![SN Step 3](images/SN3.png)

* Click Import Update Set from XML under the Related Links section.

    ![SN Step 4](images/SN4.png)

* Click Browse..

    * Find and Open the XML file that was previously downloaded.

    * Click Upload.

      ![SN Step 5](images/SN5.png)

* Thycotic Account Lifecycle Manager should now appear in the list of Retrieved Update Sets records.

* Click Thycotic Account Lifecycle Manager under the Name column to open up the record.

    ![SN Step 6](images/SN6.png)

*  Click **Preview Update Set**. An Update Set Preview dialog will appears. Click Close when it is finished.

    ![SN Step 7](images/SN7.png)
    ![SN Step 8](images/SN8.png)

* Click **Commit Update Set**. An Update Set Commit dialog will appear. Click Close when it is finished.
    
    ![SN Step 9](images/SN9.png)
    ![SN Step 10](images/SN10.png)

* **Done!** The app should now be installed in the ServiceNow instance. 
    * Reload ServiceNow in your browser.
    * Thycotic Account Lifecycle Manager should now be available in the navigation menu.
    ![SN Step 11](images/SN11.png)