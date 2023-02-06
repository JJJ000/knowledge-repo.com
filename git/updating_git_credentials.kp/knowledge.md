---
title: Change git credential helper password
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The git credential helper cannot update passwords; the user must manually reset the password.
---

**Contents**

[TOC]

## Using Command Line
1. Open the command line and type `git config --global credential.helper` to check which credential helper is currently configured.
2. If the output is `manager`, type `git credential-manager update` to update the password.

## Using Git GUI
1. Open the Git GUI and go to `Edit` > `Options` > `Credentials`
2. Select the credential helper from the drop-down menu and click `Edit`
3. Enter the new password and click `Save`
