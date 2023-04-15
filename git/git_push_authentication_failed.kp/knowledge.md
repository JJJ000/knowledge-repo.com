---
title: Pushing to git failed due to authentication issues
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Check that your credentials are correct and that you have access to the repository.
---

**Contents**

[TOC]

### Solutions

### Check SSH Key

The most common cause of an authentication failed error when using Git is that the SSH key used to authenticate with the remote repository does not match the one configured in your Git settings. To check the SSH key associated with your account, run the following command in your terminal:

```git
$ ssh-keygen -l -E md5 -f ~/.ssh/id_rsa.pub
```

This will output a long string that is the SHA-1 fingerprint of your SSH key. Compare this to the SSH key configured in your Git settings to make sure they match.

### Check Credentials

Another possible cause of an authentication failed error is that the credentials used to authenticate with the remote repository are incorrect. To check the credentials associated with your account, log into the remote repository and look for the username and password settings.

Make sure that the username and password match what you have configured in your Git settings. If they do not match, update the settings accordingly.

### Check Permissions

Finally, an authentication failed error can occur if you do not have the necessary permissions to push to the remote repository. To check your permissions, log into the remote repository and look for the user settings.

Make sure that your user has the necessary permissions to push to the repository. If not, contact the repository administrator to request the necessary permissions.
