## Login
```bash
SSH: ssh bandit6@bandit.labs.overthewire.org -p 2220
```
```bash
Password: DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```
## Task
Find a file somewhere on the server. Properties:

* owned by user bandit7
* owned by group bandit6
* 33 bytes in size

## Solution
We use the find command with the following options:

* ```-type f```: because we are looking for a file
* ```-user bandit7```: to find files owned by the ‘bandit7’ user
* ```-group bandit6```: to find files owned by the ‘bandit6’ group
* ```-size 33c```: to find files of size 33 bytes
* ```/```: run from root directory
* ```2>/dev/null```: exclude fiels that we dont have permission to / hide error messages
  
```bash
bandit6@bandit:~$ find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
```
```bash
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```
Boom! we got the password.
<hr>

[Level 8](Level%208.md)
