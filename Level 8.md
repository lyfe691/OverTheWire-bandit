## Login
```bash
SSH: ssh bandit7@bandit.labs.overthewire.org -p 2220
```
```bash
Password: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```

## Task
Get the password from a file, next to the word millionth

## Solution
Instead, we can try using grep, since the password is in the same line as the word ‘millionth’
```bash
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```
<hr>

[Level 9](Level%209.md)
