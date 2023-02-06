---
title: I am receiving an error that I do not have permission to access the gitlab repository using my public key
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Make sure the correct SSH key is added to your GitLab account.
---

**Contents**

[TOC]

# Troubleshooting Steps
1. Check if the correct SSH key is added
2. Check the permissions of the SSH key
3. Check if the SSH key is in the correct format

# Check if the Correct SSH Key is Added
In order to connect to GitLab, the correct SSH key must be added. To verify that the correct SSH key is added, follow these steps:

1. Log in to your GitLab account.
2. Navigate to your profile settings.
3. Click on the "SSH Keys" tab.
4. Verify that the correct SSH key is listed.

# Check the Permissions of the SSH Key
In order for the SSH key to be accepted, it must have the correct permissions. To verify that the SSH key has the correct permissions, follow these steps:

1. Open a terminal window.
2. Change the directory to the location of the SSH key.
3. Run the command `ls -l` to view the permissions of the file.
4. Verify that the permissions are set to `600`.

# Check if the SSH Key is in the Correct Format
In order for the SSH key to be accepted, it must be in the correct format. To verify that the SSH key is in the correct format, follow these steps:

1. Open the SSH key file in a text editor.
2. Verify that the file contains a single line that starts with "ssh-rsa".
3. Verify that the file does not contain any extra whitespace or line breaks.
