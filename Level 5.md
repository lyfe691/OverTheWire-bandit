## Login
SSH: ssh bandit4@bandit.labs.overthewire.org -p 2220

Password: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

## Task
The password for the next level is stored in the only human-readable file in the inhere directory.

## Solution
We again go into the ‘inhere’ directory and print out the files in the system:
```
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls -la
total 48
drwxr-xr-x 2 root    root    4096 May  7  2020 .
drwxr-xr-x 3 root    root    4096 May  7  2020 ..
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file00
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file01
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file02
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file03
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file04
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file05
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file06
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file07
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file08
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file09
```
We can see that there are ten files.
<hr>

We can use different methods to find the human-readable file and therefore, the password.

1. We could just print the contents of every file (cat). This is, however, not very efficient when we deal with more files.
2. Instead, we could use the method I mentioned in the theory part. The command structure is file <filename>. Instead of using a filename, we use a wildcard to get the type for all the files. Additionally, looking at the file names, specifically at the fact, the names start with ‘-’, gives us problems. Therefore we use the same method as in Level 2.

```bash
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```
We can see that only ‘-file07’ is of type ‘ASCII text’, which is one of the encodings, that humans can read. (It is also the same file type as the files from previous levels.) Now we only need to cat the file:
```bash
bandit4@bandit:~/inhere$ cat ./-file07
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```
And we get the next password.
