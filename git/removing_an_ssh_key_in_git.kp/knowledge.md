---
title: What is the process for deleting an ssh key?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To remove an SSH key in Git, run the command `ssh-keygen -R <host>`.
---

**Contents**

[TOC]

1. ##Check for Existing SSH Keys

Before you can delete an SSH key, you need to know if it exists. To check for existing SSH keys, open Git Bash and run the following command:

```
ls -al ~/.ssh
```

2. ##Delete SSH Key

Once you have identified the SSH key you want to delete, you can use the following command to delete it:

```
ssh-keygen -R <host>
```

Replace <host> with the name of the host associated with the SSH key you want to delete.

3. ##Verify SSH Key Deletion

You can verify that the SSH key has been deleted by running the following command:

```
ssh-add -l
```

If the SSH key has been successfully deleted, it will not appear in the list of SSH keys.

4. ##Update Git Config

Finally, you need to update the Git config file to remove the SSH key from the list of known hosts. Open the Git config file in a text editor and delete the line associated with the SSH key you just deleted. Save the file and you are done.
