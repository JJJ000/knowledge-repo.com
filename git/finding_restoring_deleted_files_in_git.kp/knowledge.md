---
title: What is the process for locating and restoring a file that has been removed from a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: Run `git checkout HEAD <file>` to restore the deleted file in the Git repository.
---

**Contents**

[TOC]

### Identifying the File 

The first step in restoring a deleted file in a Git repository is to identify the file that needs to be restored. To do this, you can use the `git log` command to list all commits in the repository, including any that may have deleted the file. 

The `git log` command will list the commit messages and the SHA-1 hashes for each commit. You can then use the SHA-1 hash of the commit that deleted the file to find it.

### Restoring the File

Once you have identified the commit that deleted the file, you can use the `git checkout` command to restore it. This command will check out the version of the file that was present in the commit before it was deleted.

You can use the `git checkout` command with the SHA-1 hash of the commit that deleted the file, followed by the path to the file. For example, if the SHA-1 hash of the commit that deleted the file is `abc123`, you can restore the file with the command `git checkout abc123 /path/to/file`.

### Committing the File

Once you have restored the file, you can commit it back to the repository. To do this, you can use the `git commit` command with the `-a` flag to commit all changes, or the `-m` flag to specify a commit message.

For example, if you want to commit the file with the message "Restoring deleted file", you can use the command `git commit -m "Restoring deleted file"`.

### Pushing the File

Finally, once you have committed the file, you can push it back to the remote repository with the `git push` command. This will upload the file to the remote repository, restoring it to its previous state.
