[title]: # (Installation)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,on-premise,on-prem,self hosted,install)
[priority]: # (4520)

# Installation

Create a directory to store the ALM data.
```
mkdir ~/alm
```

>**NOTE**: This directory will contain configuration files for ALM.  Permissions should be set to only necessary users. (e.g. the account that installed ALM, an account used for running backups, etc.)

## Change to that directory.

```
cd ~/alm
```

## Download and Install the Script:

```
curl https://alc-cdn01.azureedge.net/scripts/alm.sh -o alm.sh && chmod +x alm.sh && ./alm.sh install
```

## Domain name

```
What domain name will users use to access ALM?
```

To use LetsEncrypt, you’ll need a domain name that points to your public IP, and ports 80 and 443 forwarded from your router to the local IP of the machine that is running ALM.

## SSL/TLS Configuration 

```
--- SSL/TLS Configuration ---
ALM requires a SSL/TLS certificate to ensure that all web communication is secure.
ALM can be configured to use LetsEncrypt to automatically create and manage the certificate.
Or you may provide your own.

Would you like to use LetsEncrypt to generate an SSL/TLS certificate for docker.enzadev.com? [y/n]:
```
```y``` will pull the ```certbot``` container and attempt to get a certificate for the domain entered in the previous step.  The acquired certificates will be under ```./almdata/letsencrypt```

```n``` will wait for you to copy the certificate (named ```<DOMAIN>.crt```, *e.g.* ```example.alm.com.crt```) and private key (named ```<DOMAIN>.key```, *e.g.* ```example.alm.com.key```) to the same folder as the install script.  It will move them to the ```./almdata/ssl``` directory as part of the install.  

## Database Configuration

```
--- Database Configuration ---
ALM needs to set up a SQL Server database to store its data.
You can use your own SQL Server instance to host the database, 
or you may choose to have a SQL Server Express instance set up automatically as a container.

Do you want to automatically set up your database in a SQL Express container? [y/n]:

``` 
```y``` will generate credentials and move on to the next step

```n``` will prompt you for the connection info for SQL Server.  
```

  Enter the connection info for your SQL Server:
  Server:
  Database:
  User ID:
  Password:
```

## Admin User

```
--- Admin User ---
ALM requires at least one admin user.  We will configure the first admin user as part
of the installation process. This admin user will also receive email alerts regarding
LetsEncrypt certificate expirations.
Initial User Display Name: 
Initial User Email:
``` 

These are the values that will be used for the initial admin account.  Make sure you use an account that can log into the OIDC instance below.

## Authentication Configuration

```
--- Authentication Configuration ---
ALM requires an OpenID Connect (OIDC) provider for user authentication. Please provide
the credentials to your preferred OIDC provider.
OIDC Authority URL: 
OIDC Client ID: 
OIDC Client Secret: 
```

>**NOTE**: The domain you use will need to be configured as a reply url in whatever OIDC provider you use, or you will get an “invalid reply url” error when you try to log in.

## Email Configuration

```
--- Email Configuration ---
ALM uses SMTP to send email notifications to users. Please provide the SMTP credentials
to your preferred provider.
Server: 
Port: 
Use SSL?:
Use Credentials?:
(If yes, then:)
  Domain:
  User Name:
  Password:
```

>**NOTE**: Use these settings to connect to an SMTP server. These do not need to be valid to complete the install.
