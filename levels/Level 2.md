# Level 2

## Login 
```bash
SSH: ssh bandit1@bandit.labs.overthewire.org   -p 2220  
Password: `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`
```

## Task
Retrieve the password from the file named `-`.

## Solution

### Step 1: Verify the presence of the file
First, check that the file is actually in the current directory:
```bash
bandit1@bandit:~$ ls
-
```
### Step 2: Correct method to access the file
To properly read the file, you should specify the path explicitly by prepending ./ to the filename:
```bash
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```
So we got the next password.
<hr>

[Level 3](Level%203.md)
