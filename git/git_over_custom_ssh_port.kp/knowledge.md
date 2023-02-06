---
title: Connect to git using a custom ssh port
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To use a custom SSH port with Git, specify the port number in the SSH URL (e.g. git@host.comport).
---

**Contents**

[TOC]

# Section 1: Setting up SSH

In order to use Git on a custom SSH port, you must first set up an SSH connection to the server using the desired port. This can be done using the `ssh` command, with the `-p` option to specify the port.

For example, if the server is located at `example.com` and the desired port is `1234`, the command would be:

```
ssh -p 1234 user@example.com
```

# Section 2: Configuring Git

Once the SSH connection is established, the next step is to configure Git to use the custom port. This can be done by setting the `GIT_SSH_COMMAND` environment variable to use the `ssh` command with the `-p` option to specify the port.

For example, if the desired port is `1234`, the command would be:

```
export GIT_SSH_COMMAND="ssh -p 1234"
```

# Section 3: Testing the Connection

Once the SSH connection and Git configuration are complete, the connection can be tested by attempting to clone a repository from the server. This can be done using the `git clone` command, with the `--ssh` option to specify the SSH connection.

For example, if the repository is located at `example.com/repo`, the command would be:

```
git clone --ssh user@example.com:repo
```

# Section 4: Troubleshooting

If the connection fails, it is important to check the SSH connection and Git configuration for any errors. Additionally, it may be necessary to check the server's firewall settings to ensure that the desired port is open and accessible.
