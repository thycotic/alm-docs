[title]: # (Workflow Templates)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5180)

# Alert Settings

## Email Templates

Administrators can modify and enable/disable emails that are generated and sent automatically by ALM.
<table>
<tr valign="top">
<td>

To modify an **Email Template**:
1. Navigate to **Alert Settings** and click **Email Templates**. The Templates are named after the event in ALM that will trigger the Email.
1. Click the name of the Template to bring up the **Manage Email Template** page. From here you can:
    * Change the **Subject** line of the Email.
    * Change the **Body** of the Email. Use the **Parameters** variables to customize the message. You can add the Parameters by retyping them or clicking **insert**.
1. **Enable** or **Disable** the Email using the toggle. 
1. Click **Save** when you are finished. 

</td>
<td valign="top" halign="right">

![manageemail](images/manageemail.png)

</td>
</table>

## Webhooks

<table>
<tr valign="top">
<td>

ALM allows Administrators to set up custom integrations using webhooks. To create a webhook:
1. Navigate to **Alert Settings** and click **Webhooks**.
1. In the upper right-hand corner, click **Create Webhook** to bring up the **Add Webhook** window.
1. Enter a description of the webhook.
1. Choose the **Event** within ALM that will trigger the webhook.
1. Click **Save** to bring up the **Manage Webhook** page. 
    > **Note**: The webhook will not be created until after setup is completed.

</td>

<td halign="right">

![webhook1](images/addwebhook1.png)

</td>
</tr>

<tr valign="top">

<td>

6. On the **Manage Webhook** page, enter the complete **Callback** URL. The **Message Body** shows the data that will be sent to the URL.
1. Check the box next to **Enabled** to activate the webhook. Leave the box unchecked to keep the webhook inactive. It can be enabled later from this page.
1. Click **Save** to create the webhook.
1. Once the webhook is created and enabled, you can view its usage details from the **Webhook History** tab at the top of the page. 

</td>

<td halign="right">

![webhook2](images/addwebhook2.png)

</td>