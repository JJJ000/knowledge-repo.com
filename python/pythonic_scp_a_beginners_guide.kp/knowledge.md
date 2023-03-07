---
title: What is the process for using scp in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can use the paramiko module to scp files in Python.
---

**Contents**

[TOC]

Section 1: Overview

SCP or Secure Copy Protocol is a network protocol used to securely transfer files between remote system and local system. Python provides various modules to implement SCP for file transfer. This article provides an overview of using SCP in Python and covers sections like prerequisites and installation, establishing SSH connection, file transfer and closing the connection.

Section 2: Prerequisites and Installation

Before we get started with the SCP implementation in Python, we should have the following prerequisites installed on our system:

1. Python
2. Paramiko library

Python comes preinstalled on most modern operating systems, however Paramiko library needs to be installed separately. Paramiko is a Python implementation of SSH with both client and server functionality. You can install Paramiko using pip package manager by executing the following command:

```
pip install paramiko
```

Section 3: Establishing SSH Connection

In order to perform SCP in Python, we first need to establish an SSH connection between the local system and the remote system. We can establish an SSH connection using the Paramiko library in Python. Below code snippet shows how to establish an SSH connection and authenticate with the remote system:

```python
import paramiko

# Remote system details
HOSTNAME = "example.com"
PORT = 22
USERNAME = "user"
PASSWORD = "secret"

# Initiate SSH client
ssh = paramiko.SSHClient()
ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy())

# Connect to the remote server
ssh.connect(HOSTNAME, PORT, USERNAME, PASSWORD)

# SCP usage goes here...

# Close the SSH client
ssh.close()
```

Section 4: File Transfer

Once the SSH connection is established, we can use SCP to transfer files between the remote system and the local system. Paramiko library provides the SCPClient class to perform SCP in Python. Below code snippet shows how to use SCPClient to transfer files between local and remote systems:

```python
import paramiko
from scp import SCPClient

# Remote system details
HOSTNAME = "example.com"
PORT = 22
USERNAME = "user"
PASSWORD = "secret"

# Initiate SSH client
ssh = paramiko.SSHClient()
ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy())

# Connect to the remote server
ssh.connect(HOSTNAME, PORT, USERNAME, PASSWORD)

# Create SCP client
scp = SCPClient(ssh.get_transport())

# Transfer file from local system to remote system
scp.put('local_file.txt', '/remote_file.txt')

# Transfer file from remote system to local system
scp.get('/remote_file.txt', 'local_file.txt')

# Close the SCP client
scp.close()

# Close the SSH client
ssh.close()
```

Section 5: Closing the Connection

After the file transfer is complete, we should close the SCP client and the SSH client. Closing the SCP client and SSH client ensures that the resources are released and the connections are closed properly.

```python
# Close the SCP client
scp.close()

# Close the SSH client
ssh.close()
```

Conclusion

In conclusion, SCP implementation in Python can be done using the Paramiko library. It provides the SCPClient class to perform SCP operations over SSH connections. This article covered the prerequisites and installation, establishing SSH connection, file transfer, and closing the connection.
