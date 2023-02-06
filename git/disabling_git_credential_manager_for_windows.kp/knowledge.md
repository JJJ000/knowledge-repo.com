---
title: What is the process for turning off git credential manager for windows?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run the command `git config --system --unset credential.helper` to disable Git Credential Manager for Windows.
---

**Contents**

[TOC]

# Section 1: Uninstall Git Credential Manager
1. Open the Control Panel.
2. Select Programs > Uninstall a Program.
3. Select Git Credential Manager and click Uninstall.

# Section 2: Unregister the Git Credential Manager
1. Open a command prompt.
2. Run `git config --system --unset credential.helper`.

# Section 3: Remove Cached Credentials
1. Open the Windows Credential Manager.
2. Select "Windows Credentials" and remove any credentials associated with Git.

# Section 4: Verify
1. Open a command prompt.
2. Run `git config --system --list` to verify that the credential.helper setting has been removed.
