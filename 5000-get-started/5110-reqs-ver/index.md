﻿[title]: # (Requirements Verification)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (5110)

# Requirements Verification 

Being a cloud service, ALM requires no boxed software installation. 

* However, to successfully use ALM from access points within your enterprise requires that your organization’s IT infrastructure meet several criteria.

* Additionally, ALM as provisioned requires initial setup and configuration steps to correctly connect to your organization’s enterprise architecture.

Neither onerous nor time consuming, these steps do justify advance consideration, and most require elevated privileges in ALM or on your corporate domain.

## Thycotic One accounts

Each member of your organization who will use ALM must have a **Thycotic One** account. These free accounts provide authentication to Thycotic’s cloud services.

To open a Thycotic One account, visit *login.thycotic.com*.

The email a user submits when signing up for Thycotic One determines the email they must provide when obtaining an ALM user account.

## Suitable Browsers

ALM supports Google Chrome and Mozilla Firefox.

## Thycotic Secret Server

ALM uses Secret Server to store credentials for the accounts it creates in Active Directory. This removes security risks long associated with storage of the temporary credentials for new AD accounts.

If you are not using Secret Server Cloud, your Secret Server version must be Version 10.2.000018 or later with the Secret Server Platinum license or the API Add-on. Secret Server’s web services must be running.

Instructions related to Secret Server requirements appear in [Integrate ALM with Secret Server](../5120-integ-secret-serv/).

## An Active Directory Installation

You must have an Active Directory Domain Controller on **Windows Server 2012** or later, *or* **Azure AD Domain Services** and a user account with the privileges to create an AD account for ALM to use that will be privileged, itself, to create accounts in AD. ALM will authenticate to Active Directory using that account.

* ALM users create proxies for new Active Directory service accounts in ALM, and ALM replicates these in Active Directory, creating the actual service accounts.

* ALM supports only Active Directory, but future releases may support other directory services.

For details on integration with Active Directory, see [Integrate ALM with Active Directory](../5130-integ-active-dir/).

## Remote Worker Windows Service

Often initially misunderstood as an actual staff member, the Remote Worker is nothing more than a Windows Service that runs on a machine in your organization’s environment.

* In software jargon, a “worker” is a process or service running in some degree independently of the main body of software to which it belongs, and used to perform tasks the main body of software cannot perform for itself.

In the case of ALM, the Remote Worker is a Windows Service that runs on your organization’s hardware. It manages interactions between the ALM cloud service and your Active Directory installation. It also supports ALM’s integration with your organization’s Secret Server instance.

See [Setup the Remote Worker Service](../5140-setup-remote-wrk) for details.

![Article End](../../alm-bug.png)

  

  