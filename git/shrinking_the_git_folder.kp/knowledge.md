---
title: Decrease the size of the .git folder
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The .git folder cannot be shrunk.
---

**Contents**

[TOC]

# Section 1: Understanding the .git Folder

The .git folder is a hidden folder in the root directory of a repository. It is the most important part of a Git repository, as it contains the entire history of the repository, including the commits, branches, and other version control data.

# Section 2: Shrinking the .git Folder

The .git folder can become very large over time, as it accumulates more and more data. To shrink the .git folder, you can use the `git gc` command. This command will clean up unnecessary files and optimize the repository for better performance.

# Section 3: Optimizing the .git Folder

In addition to running the `git gc` command, you can also optimize the .git folder by compressing it. This can be done by running the `git repack` command, which will compress the .git folder and make it smaller.

# Section 4: Verifying the Size of the .git Folder

Once you have optimized and compressed the .git folder, you can verify its size using the `du` command. This will show you the total size of the .git folder and its contents.
