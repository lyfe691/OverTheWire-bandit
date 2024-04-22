# Level 3
## Login
```bash
SSH: ssh bandit2@bandit.labs.overthewire.org -p 2220
```
```bash
Password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```

## Task
The password for the next level is stored in a file called spaces in this filename located in the home directory.

## Solution
Similar to the previous level, simply trying to use the filename does not work:
```
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
```
This is because it assumes that we look at four files (or directories), which, however, do not exist.

Instead, we need to surround names with spaces with quotes (single or double) to indicate that all of it belongs to the name for one file:

```bash
bandit2@bandit:~$ cat \spaces\ in\ this\ filename\
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```
And we can read the file and get the next password.
<hr>

[Level 4](Level%204.md)
