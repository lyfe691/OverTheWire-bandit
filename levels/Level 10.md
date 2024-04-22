## Login
```bash
SSH: ssh bandit9@bandit.labs.overthewire.org -p 2220
Password: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

## Task
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## Solution
```bash
bandit9@bandit:~$ strings data.txt | grep ===
========== the*2i"4
========== password
Z)========== is
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```
<hr>

[Level 11](Level%2011.md)
