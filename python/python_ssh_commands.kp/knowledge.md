---
title: Execute Python commands remotely over ssh
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can perform commands over SSH with Python using the paramiko library.
---

**Contents**

[TOC]

Connecting to SSH with Python
---

To connect to an SSH server using Python, we need to use the paramiko library. Paramiko is a Python library that provides SSH protocol implementation for client and server applications. Here is how to connect to SSH using Python:

```python
import paramiko

ssh = paramiko.SSHClient()
ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy()) # Make the script accept the ssh key automatically
ssh.connect(hostname='server-ip', username='username', password='password')
```
 
Here, we first import the paramiko library, and then create an SSH object. We then tell the object to automatically accept the ssh key if it is not known, to prevent security errors. Finally, we use the connect() method to establish the connection to the SSH server


Running commands over SSH with Python
---

Once we have established an SSH connection, we can run any command on the remote system using Python. Here’s an example of how to run a command:

```python
stdin, stdout, stderr = ssh.exec_command('ls -l')
output = stdout.read()
if output:
    print('Command output:', output.decode('utf-8'))
```

In the above example, we have used the exec_command method of the SSH object to run the `ls -l` command on the remote system. This method returns a tuple of standard input, standard output, and standard error, which we capture in the variables stdin, stdout, and stderr. We then read the standard output buffer and print the command output.

Uploading files via SSH with Python
---

We can also use the paramiko library to upload files over SSH using Python. Here is how to upload a local file to a remote system using SSH:

```python
import paramiko

ssh = paramiko.SSHClient()
ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy()) 
ssh.connect(hostname='server-ip', username='username', password='password')

sftp = ssh.open_sftp()

local_path = './local_file.txt'
remote_path = '/home/user/remote_file.txt'

sftp.put(local_path, remote_path)

sftp.close()
```

In the above example, we first establish an SSH connection and create an SFTP object using the open_sftp method. We then set the local and remote file paths and use the put() method of the SFTP object to upload the local file to the remote system. Finally, we close the SFTP connection.

Downloading files via SSH with Python
---

Similarly, we can download files over SSH using Python. Here’s how to download a remote file to a local system using SSH:

```python
import paramiko

ssh = paramiko.SSHClient()
ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy()) 
ssh.connect(hostname='server-ip', username='username', password='password')

sftp = ssh.open_sftp()

local_path = './local_file.txt'
remote_path = '/home/user/remote_file.txt'

sftp.get(remote_path, local_path)

sftp.close()
```

In the above example, we first establish an SSH connection and create an SFTP object using the open_sftp method. We then set the local and remote file paths and use the get() method of the SFTP object to download the remote file to the local system. Finally, we close the SFTP connection.
