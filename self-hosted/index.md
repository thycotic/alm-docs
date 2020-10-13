[title]: # (Self-Hosted)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,on-premise,on-prem,self hosted)
[priority]: # (3500)


# Prerequisites

The following are required to install the self-hosted version of ALM:

1. **Linux Machine**
    >**NOTE**: Tested against the following - Ubuntu 16.04, Ubuntu 18.04, Debian 9, Debian 10, CentOS 8.2, Fedora 32.
1. **Docker**
    * Manages the images and containers used by ALM.
    * Installation Instructions : https://docs.docker.com/get-docker/
1. **Docker Compose**
    * This is required for ALM’s installation script to manage the local orchestration of services.
    * Installation instructions: https://docs.docker.com/compose/install/
1. **Port Configuration**
    * After installation, the docker containers will require the following ports to be available on the host system:
        * TCP/80, if LetsEncrypt certificate management is enabled.
        * TCP/443 for the web UI.

# Additional Requirements

During installation and configuration, you will need to know the following ahead of time:

* **Domain** (Example: alm.thycotic.com)
  * Site where ALM will accessible to users through a web browser.
* **SSL/TLS Certificate for the domain** 
  * Can be managed automatically using LetsEncrypt, as an option.
  * Or a certificate and chain can be provided manually during setup.
* **Open ID Connect (OIDC) credentials**
  * ALM uses OIDC for user authentication.
  * This can be configured through Azure Active Directory or Thycotic One.
* **SMTP credentials** (*optional*) - Allows ALM to send email notifications to users.  If you choose to not use SMTP, put in any values for the questions and please understand email notifications will not be sent in ALM. This can be re-configured in the future by running ```./alm.sh install```, this will initiate the install process again but exclude initial user configuration.
