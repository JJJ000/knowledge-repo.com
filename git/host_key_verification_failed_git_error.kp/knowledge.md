---
title: When attempting to connect to a remote repository, an error occurred stating "host key verification failed"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: This error occurs when the SSH key for the remote repository is not recognized by the local machine.
---

**Contents**

[TOC]

### Solution 1: Check Host Key

1. Use the `ssh-keygen -F <hostname>` command to check if the host key of the remote repository exists in the `known_hosts` file.
2. If the host key is present, then delete it using the `ssh-keygen -R <hostname>` command.
3. Then try to connect to the remote repository again.

### Solution 2: Disable Host Key Checking

1. Edit the `~/.ssh/config` file and add the below lines:

```git
Host <hostname>
    StrictHostKeyChecking no
    UserKnownHostsFile /dev/null
```

2. Save the file and try to connect to the remote repository again.

### Solution 3: Use SSH Keys

1. Generate an SSH key pair using the `ssh-keygen` command.
2. Add the public key to the remote repository.
3. Connect to the remote repository using the private key.

### Solution 4: Use the SSH Agent

1. Start the SSH Agent using the `ssh-agent` command.
2. Add the private key to the SSH Agent using the `ssh-add` command.
3. Connect to the remote repository.
