# Bandit Level 5 → 6 

#### Task

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable

### Commands used:

* **cd (Change Directory):** Used to move from one folder to another to navigate the file system and access different directories.

* **find:** A powerful utility used to search for files in a directory hierarchy based on specific attributes like size, type, and permissions.

* **cat:** Short for "concatenate," used to read and display the text content of a file directly in the terminal.

### Solution:

1. Move into the target directory mentioned in the task:
```bash
cd inhere
```

2. Use the find command to search for a file that matches the three specific criteria mentioned in the task:
```bash
find . -type f -size 1033c ! -executable
```
* **.:** tells the command to search the current location and all subdirectories.

* **-type f:** filters for regular files.

* **-size 1033c:** filters for files exactly 1033 bytes in size.

* **! -executable:** This acts as a NOT filter; it excludes any files that have execution permissions and only shows files that are not executable.

3. The command will return a specific path. Read that file to get the password:
```bash
cat ./maybehere07/.file2
```


Key Concepts Learned
------

* **Advanced Searching:** The find command is essential for locating files when you don't know the filename but know its characteristics like size or type.

* **The NOT Operator (!):** Placing ! before a condition inverts the logic. In this case, ! -executable means "find files where executable permission is NOT present."

* **Size Specifiers:** In the find command, c is used for bytes. Using the exact byte count helps narrow down a single file out of hundreds.
