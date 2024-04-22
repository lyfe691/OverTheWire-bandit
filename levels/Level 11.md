# Level 11
## Login
```bash
SSH: ssh bandit10@bandit.labs.overthewire.org -p 2220
Password: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```

## Task
The password for the next level is stored in the file data.txt, which contains base64 encoded data.

## Solution
The base64 command allows files as input, so we just need to use the command on the file.

```bash
bandit10@bandit:~$ base64 -d data.txt
Thepassword is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```
<hr>

[Level 12](Level%2012.md)
