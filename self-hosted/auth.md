[title]: # (Auth0 Configuration)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,on-premise,on-prem,self hosted,auth0)
[priority]: # (3540)

# Configure Auth0 Open ID Connect (OIDC)

## Create An Application in Auth0

The Auth0 application will allow for authentication with ALM.

1. Sign into [Auth0](https://auth0.com) or create an account.
1. Navigate to **Applications**

    ![auth-step1](images/auth-step1.png "getting started")

1. Click **Create Application**.
    * Provide a **Name**.
    * Under **Choose an application type** select **Regular Web**.
    * Click **Create**.
    ![auth-step2](images/auth-step2.png "applications")
    ![auth-step3](images/auth-step3.png "create application")

## Copy Domain/Client ID/Client Secret

After the application is created, find and copy the values that will be needed during the ALM setup.

1. Select the **Settings** tab.
1. Under **Basic Information**, make note of the following:
    * **Domain**- This will be the OIDC Authority URL value during setup.
    * **Client ID**
    * **Client Secret**

    ![auth-step4](images/auth-step4.png "settings tab")
    ![auth-step5](images/auth-step5a.png "basic information")

## Configure Settings 

While in the Settings section, configure the settings that are specific to your self-hosted instance.

1. Scroll down to the **Applications URIs** section and fill out the following fields
    * **Application Login URI** - ```https//{{your ALM Domain}}```
    * **Allowed Callback URLs** - ```https://{{your ALM Domain}}/signin-oidc,https://{{your ALM Domain}}/signout-callback-oidc```
    * **Allowed Logout URLs** - ```https://{{your ALM Domain}}/authentication/logout```
    ![auth-step6](images/auth-step5.png "configure")

1. Scroll to the bottom of the page and click **Save Changes.**
