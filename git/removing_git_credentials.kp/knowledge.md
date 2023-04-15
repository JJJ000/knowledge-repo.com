---
title: Delete credentials from git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run the `git credential-osxkeychain erase` command to remove credentials from Git.
---

**Contents**

[TOC]

### Remove Credentials from Git

### Check for Credentials

To check if your Git credentials are stored in the Windows Credential Manager, open the Control Panel and search for "Credential Manager". Select the "Windows Credentials" option and look for any credentials related to Git or your repository.

### Modify the Credentials

If you find any credentials related to Git, select the credential and click "Edit". This will open a window where you can modify the username and password. Change the username and password to something that is not related to your Git repository and click "OK".

### Remove the Credentials

If you no longer need the credentials, you can remove them by selecting the credential and clicking "Remove". This will permanently delete the credential from the Windows Credential Manager.

### Clear Credentials from Git

Finally, you can clear any stored credentials from Git by running the following command:

```git
git config --global --unset credential.helper
```

This will remove any stored credentials from Git and prevent them from being used in the future.
