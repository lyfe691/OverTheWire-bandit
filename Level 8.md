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
Checking the file size of data.txt, we can see it is huge:

bandit7@bandit:~$ du -b data.txt 
4184396 data.txt
So simply looking through the file, would take too long and be too much effort.

Instead, we can try using grep, since the password is in the same line as the word ‘millionth’

1
2
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV
