# Bandit Level 6 → 7

#### Task

The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size

### Commands used:

* **find:** A powerful utility used to search for files in a directory hierarchy based on specific attributes like ownership, group, and size.

* **cat:** Short for "concatenate," used to read and display the text content of a file directly in the terminal.

* **2>/dev/null:** A redirection technique used to suppress error messages (like "Permission denied") by sending them to a virtual "null" device.

### Solution:

1. Use the find command to search the entire file system (starting from root /) for a file matching the specific ownership and size criteria:
```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

**/** tells the command to search the entire system starting from the root.

**-user bandit7** filters for files owned by the user bandit7.

**-group bandit6** filters for files owned by the group bandit6.

**-size 33c** filters for files exactly 33 bytes in size.

**2>/dev/null** ensures that the output is clean by hiding hundreds of "Permission denied" errors.

2. The command returns a single path. Read that file to reveal the password:
```bash
cat /var/lib/dpkg/info/bandit7.password
```


Key Concepts Learned
------

* **System-Wide Searching:** Searching from the root directory (/) allows you to find files anywhere on the server, not just in your home directory.

* **Ownership Filters:** The find command can filter files based on which User (-user) or Group (-group) owns them, which is critical for security auditing.

* **Error Redirection:** In Linux, 2> refers to the "Standard Error" stream. Redirecting it to /dev/null (the "black hole") is a common way to clean up command output.
