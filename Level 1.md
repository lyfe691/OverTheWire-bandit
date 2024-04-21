
## Task
The password for the next level is stored in a file called readme located in the home directory.
## Login
```bash
SSH: ssh bandit0@bandit.labs.overthewire.org -p 2220
```
```bash
Password: bandit0
```

## Solution




Make sure readme file is in the directory
```bash
bandit0@bandit:~$ ls
```
Since this is the case, we can print the content of a file with the following command syntax: cat 'yourfile'.
```bash
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```
The resulting string is the password for the ‘bandit1’ user.

[Level 2](Level%202.md)
