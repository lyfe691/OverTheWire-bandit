# Level 14
## Login
```bash
SSH: ssh bandit13@bandit.labs.overthewire.org -p 2220
Password: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```

## Task
The password for the next level is stored in ```/etc/bandit_pass/bandit14``` and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level.

## Solution
I logged into the server as bandit13 and found the file ‘sshkey.private’ in the home directory. Knowing the location of the file, I can transfer it to my machine.
```bash
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
```
I used scp to connect to the remote machine and get the ssh key.
```bash
┌──(lyfe㉿kali)-[~]
└─$ scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .         
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit13@bandit.labs.overthewire.org's password: 
sshkey.private
```
Now that I had the private ssh key, I tried to log in with it. However, I got the following warning Permissions 0640 for 'sshkey.private' are too open., because it had the following writing permissions: -rw-r-----. So I reduced the permissions with chmod 700 sshkey.private, so only the owner (me) has permissions for the file. The permissions will then look like this: -rwx------. And now it is possible to use the key to log into the new level:
```bash
┌──(lyfe㉿kali)-[~]
└─$ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```
And we got into the server as bandit14.
<hr>

[Level 15](Level%2015.md)
