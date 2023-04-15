---
title: How can I rename a directory correctly in a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To rename a directory in a Git repository, use the `git mv` command.
---

**Contents**

[TOC]

1. **Backup the Directory:** 
   Before renaming the directory, it is important to backup the directory to ensure that no data is lost. This can be done by running the command `git checkout-index -a -f --prefix=<backup_directory>/` in the root of the repository.

2. **Rename the Directory:**
   Once the directory is backed up, the directory can be renamed using the `mv` command.

3. **Stage the Rename:**
   After the directory is renamed, the rename must be staged in the repository by running the command `git add -A <renamed_directory>`.

4. **Commit the Rename:**
   Finally, the directory rename must be committed to the repository by running the command `git commit -m "Renamed directory"`.
