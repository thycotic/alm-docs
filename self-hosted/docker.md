[title]: # (Docker Configuration)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,on-premise,on-prem,self hosted,docker)
[priority]: # (3510)

# Docker Configuration

Once Docker has been installed, add your user to the docker group. This allows the ALM setup script to run docker commands without sudo:

```
sudo groupadd docker
sudo gpasswd -a $USER docker
sudo service docker restart
```

>**NOTE**: Log out and back in for the change to take effect.