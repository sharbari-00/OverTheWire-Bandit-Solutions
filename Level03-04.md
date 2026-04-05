# Bandit Level 3 → 4

#### Task

The password for the next level is stored in a hidden file in the inhere directory located in the home directory.

### Commands used:

* **cd (Change Directory):** Used to move from one folder to another to navigate the file system and access different directories.

* **ls -a (List All):** Used to list all directory contents, including hidden files (those starting with a dot .) that are normally invisible.

* **cat:** Short for "concatenate," used to read and display the text content of a file directly in the terminal.

### Solution:

1. Move into the target directory mentioned in the task:
```bash
cd inhere
```

2. List all files (including hidden ones) to find the password file:
```bash
ls -a
```
# The output shows: .  ..  ...Hiding-From-You


3. Read the specific hidden file found in the list (ignoring the . and .. directory markers):
```bash
cat ...Hiding-From-You
```


Key Concepts Learned
------

* **Directory Markers:** In Linux, . refers to the current folder and .. refers to the parent folder. These are not files and cannot be read using the cat command.

* **Hidden Filenames:** Any file starting with a dot (.) is hidden. This file was named ...Hiding-From-You to blend in with the directory markers.

* **Multiple Arguments:** When spaces are used between names in a command like cat, Linux treats each name as a separate file or folder.

