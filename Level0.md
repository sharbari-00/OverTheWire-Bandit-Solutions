# Bandit Level 0

### Task
The objective is to establish a secure remote connection to the OverTheWire game server using the SSH protocol.

###  Connection Details
* **Host:** `bandit.labs.overthewire.org`
* **Port:** `2220`
* **Username:** `bandit0`
* **Password:** `bandit0`

###  Solution Command
Open terminal and execute the following command:
=======
### Solution
* **Host:** bandit.labs.overthewire.org
* **Port:** 2220
* **User:** bandit0
* **Password:** bandit0

### Command used:
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

  Note: use the -p flag because the server is listening on a non-standard port (2220) instead of the default SSH port (22).

Key concepts Learned
SSH (Secure Shell): A cryptographic network protocol for operating network services securely over an unsecured network.

Port Forwarding/Specification: Understanding that services don't always run on default ports.


