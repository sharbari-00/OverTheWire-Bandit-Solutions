# Bandit Level 4 → 5 

#### Task

The password for the next level is stored in the only human-readable file in the inhere directory.

### Commands used:

* **cd (Change Directory):** Used to move from one folder to another to navigate the file system and access different directories.

* **ls (List):** Used to list directory contents to see what files and dolders are available in the current directory.

* **file:** Used to determine the type of data contained within a file (e.g., ASCII text, data, or executable).

* **cat:** Short for "concatenate," used to read and display the text content of a file directly in the terminal.

### Solution:

1. Move into the target directory mentioned in the task:
```bash
cd inhere
```

2. List all files that are available in the inhere directory.
```bash
ls
```

3. Use the file command with a wildcard (*) to check the type of every file in the folder. We use ./ because the filenames start with dashes:
```bash
file ./*
```

The output revealed that ./-file07 is the only file containing ASCII text.

4. Read the identified file to reveal the password:
```bash
cat ./-file07
```

Key Concepts Learned
------

* **Data vs. Text:** Not all files contain readable text. The file command is essential for identifying "Human-Readable" (ASCII) vs. "Machine-Readable" (Binary/Data) files.

* **Wildcards:** The * symbol acts as a placeholder for "everything," allowing you to run a command on all files in a folder at once.

* **Terminal Reset:** If you accidentally cat a binary file and your terminal shows strange symbols, typing reset fixes the display.
