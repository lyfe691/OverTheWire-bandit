# Level 12
## Login
```bash
SSH: ssh bandit11@bandit.labs.overthewire.org -p 2220
Password: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```
## Task
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

## Solution
There are a lot of websites that offer ROT13 encryption/decryption, but sadly there is no build-in ROT13 command in Linux. However, I wanted a solution for the terminal, so I used the tr command for substitution.

The substitution for ROT13 is A->N,…,Z->M. With tr would be:
```bash
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```
<hr>

[Level 13](Level%2013.md)
