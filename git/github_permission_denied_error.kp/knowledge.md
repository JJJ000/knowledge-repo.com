---
title: Permission to access github was denied due to an invalid public key. unexpectedly, the connection to the remote server was terminated
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The public SSH key used to authenticate the connection is not valid or has not been added to the GitHub account.
---

**Contents**

[TOC]

# Solution 1

## Check SSH Keys

The most common cause of this issue is that the SSH key associated with the account does not have sufficient permissions. To verify that the SSH key is correctly configured, run the following command:

```
ssh -T git@github.com
```

If the output is `Permission denied (publickey)`, then the SSH key needs to be updated or re-generated.

# Solution 2

## Check GitHub Permissions

If the SSH key is correctly configured, then the issue may be related to the user's GitHub permissions. To verify that the user has sufficient permissions, go to the user's Settings page and check the permissions for the repository.

If the user does not have sufficient permissions, the user can request access from the repository owner.

# Solution 3

## Check Local Configuration

If the SSH key and GitHub permissions are correctly configured, then the issue may be related to the local configuration. To check the local configuration, run the following command:

```
git config --list
```

If the output shows any entries related to GitHub, then the user may need to update or reset the configuration.

# Solution 4

## Check Firewall

If all of the above solutions fail, then the issue may be related to a firewall or network configuration. To check if this is the case, try connecting to the repository from a different network or disable the firewall temporarily.
