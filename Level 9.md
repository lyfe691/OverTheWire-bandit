## Login
```bash
SSH: ssh bandit8@bandit.labs.overthewire.org -p 2220
Password: cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```
## Task
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.

## Solution
To find the line that occurs only once in the file, we first sort the lines and then filter for the unique one.
```bash
bandit8@bandit:~$ sort data.txt | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```
<hr>

[Level 10](Level%2010.md)
