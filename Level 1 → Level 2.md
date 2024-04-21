# OverTheWire: Bandit Level 1 → Level 2 Guide
Welcome to my guide for the Bandit Level 1 → Level 2 of the OverTheWire wargames.
## Task
The password for the next level is stored in a file called readme located in the home directory.
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
