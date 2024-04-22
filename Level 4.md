## Login
```bash
SSH: ssh bandit3@bandit.labs.overthewire.org -p 2220
```
```bash
Password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```

## Task
The password for the next level is stored in a hidden file in the inhere directory.

## Solution
#### With Traversal
First, we go to the correct folder and then print all its files to find the filename.
```bash
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
```
Therefore our file with the password is called .hidden, and we can read its content.


```bash
bandit3@bandit:~/inhere$ cat .hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
```
And we got the password for the bandit4 user.

#### Without Traversal
Alternatively, this task could be done without directory traversal by adjusting the path of both the ls and the cat command:
```bash
bandit3@bandit:~$ ls -a \inhere
.  ..  .hidden
```
```bash
bandit3@bandit:~$ cat inhere/.hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
```
And we got the password for the bandit4 user.

[Level 5](Level%205.md)
