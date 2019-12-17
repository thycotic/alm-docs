[title]: # (Requirements Verification)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (5110)

# Requirements Verification 

Successful use of ALM requires that your organization’s IT infrastructure meet several criteria.

## Thycotic One accounts

Each member of your organization who will use ALM must have a **Thycotic One** account. These free accounts provide authentication to Thycotic’s cloud services, including ALM.

To open a Thycotic One account, visit [Thycotic One](https://login.thycotic.com/Account/Login).

The email a User submits when signing up for Thycotic One will be the email they must provide later when obtaining an ALM User account.

## Suitable Browsers

ALM supports Google Chrome and Mozilla Firefox.

## Thycotic Secret Server

ALM uses Secret Server to store credentials for the accounts it creates in Active Directory. This removes security risks long associated with storage of the temporary credentials for new AD accounts.

If you are not using Secret Server Cloud, your Secret Server version must be Version 10.2.000018 or later with the Secret Server Platinum or Pro license. Secret Server’s web services must be running.

Instructions related to Secret Server requirements appear in [Integrate ALM with Secret Server](../integ-secret-serv/).

## An Active Directory Installation

You must have an Active Directory Domain Controller on **Windows Server 2012** or later, *or* **Azure AD Domain Services** and a User account with the privileges to create an AD account (for ALM to use) that will be privileged, itself, to create accounts in AD. ALM will authenticate to Active Directory using that account.

* ALM Users create proxies for new Active Directory service accounts in ALM, and ALM replicates these in Active Directory, creating the actual service accounts.

* ALM supports only Active Directory, but future releases may support other directory services.

For details on integration with Active Directory, see [Integrate ALM with Active Directory](../integ-active-dir/).

## ALM Engine Windows Service

Often initially misunderstood as an actual staff member, the ALM Engine is a Windows Service that runs on a machine in your organization’s environment.

* In software jargon, a “worker” is a process or service that runs to a large degree independently of the main body of software to which it belongs, and that performs tasks the main body of software cannot perform for itself.

In the case of ALM, the ALM Engine Windows Service runs on your organization’s hardware. It manages interactions between the ALM cloud service and your Active Directory installation. It also supports ALM’s integration with your organization’s Secret Server instance.

See [Setup the ALM Engine Service](../setup-alm-engine/) for details.



  

  
