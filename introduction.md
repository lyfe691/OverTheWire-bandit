# Introduction
The Bandit wargame is aimed at absolute beginners. It will teach the basics needed to be able to play other wargames.

### Need to know
The password you get after finishing a Level is the password you'll use for the next ssh login.

#### For example:

Your previous ssh login: ```ssh bandit0@bandit.labs.overthewire.org -p 2220```

Your new ssh login after you found the password of the level: ```ssh bandit1@bandit.labs.overthewire.org -p 2220```

### Note for VMs: 
You may fail to connect to overthewire.org via SSH with a “broken pipe error” when the network adapter for the VM is configured to use NAT mode. Adding the setting IPQoS throughput to /etc/ssh/ssh_config should resolve the issue. If this does not solve your issue, the only option then is to change the adapter to Bridged mode.
### Start
⇒ [Level 0](levels/Level%200.md)
