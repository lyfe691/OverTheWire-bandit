## Login
```bash
SSH: ssh bandit5@bandit.labs.overthewire.org -p 2220
```
```bash
Password: koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```

## Task
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

* human-readable
* 1033 bytes in size
* not executable

## Solution
1. **Navigate to the "inhere" directory:**

   ```bash
   cd inhere
    ```
Use the  ```find```command to locate the file with the specified properties:The file you're looking for is human-readable, 1033 bytes in size, and not executable.
 ```bash
find . -type f -size 1033c ! -executable
 ```
Explanation of the find command options:

* ```.``` : Searches the current directory and all subdirectories.
* ```-type f``` : Restricts the search to files only.
* ```-size 1033c``` : Looks for files that are exactly 1033 bytes in size (c stands for bytes).
* ```! -executable``` : Excludes files that are executable.

```bash
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```
<hr>

[Level 7](Level%207.md)
