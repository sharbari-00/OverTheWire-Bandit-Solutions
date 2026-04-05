# Bandit Level 2 ->3 

### Task
The password for the next level is stored in a file called --spaces in this filename-- located in the home directory

### Commands used:
* **ls (List):** Used to list directory contents to see what files and folders are available in the location.
* **cat:** Short for "concatenate," used to read and display the text content of a file directly in the terminal.
* **./ (Current Directory Reference):** Used to specify the path to a file to avoid confusion with command flags.
* **Quotes (" "):** Used to wrap filenames that contain spaces so the shell treats them as a single argument.

### Solution:

1. List the files in the home directory to confirm the --spaces in this filename-- file exists:
```bash
ls
```
2. Read the file by combining the path prefix and quotes to handle both the dashes and the spaces.
```bash
cat ./--spaces in this filename--
```


Key concepts Learned
------

* **Special Characters in Filenames:** Files starting with dashes require a path prefix (like ./) so the shell doesn't treat the filename as a command option/flag.Using ./ is a "trick" to bypass this.
* **Relative Path:** Using ./ refers to the directory you are currently standing in. 
* **Handling Spaces:** Wrapping a multi-word filename in quotes ensures the shell processes it as one single item.
