# Bandit Level 1 -> 2

### Task
The password for the next level is stored in a file called - located in the home directory.

### Commands used:
* **ls (List):** Used to list directory contents to see what files and folders are available in your current location.
* **cat:** Short for "concatenate," used to read and display the text content of a file directly in the terminal.
* **./ (Current Directory):** Used to specify the path to a file to avoid confusion with command flags.
### Solution:

1. List the files to confirm the - file exists:
```bash
ls
```
2. Read the file using relative path:
```bash
cat ./-
```

Note: Simply typing cat - will not work as the terminal interprets the dash as a special character/standard input.


Key concepts Learned
------

* **Special Characters in Filenames:** Files starting with dashes require a path prefix (like ./) so the shell doesn't treat the filename as a command option/flag.
* **Relative Path:** Using ./ refers to the directory you are currently standing in. 
