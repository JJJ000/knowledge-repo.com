---
title: What steps can I take to make diff behave like git-diff?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Set the environment variable DIFF to the path of the git-diff executable.
---

**Contents**

[TOC]

# Section 1: Install Git

In order to get diff working like git-diff, you will first need to install Git on your system. You can download the latest version of Git from the [Git website](https://git-scm.com/).

# Section 2: Configure Diff

Once you have installed Git, you will need to configure diff to work like git-diff. To do this, you will need to open up the terminal and type in the following command:

```
git config --global diff.tool git-diff
```

# Section 3: Use Diff

Once you have configured diff to work like git-diff, you can now use diff to compare two files or directories. To do this, you will need to open up the terminal and type in the following command:

```
git diff <path-to-file-or-directory1> <path-to-file-or-directory2>
```

# Section 4: View the Output

Once you have run the command, you will be presented with the output of the diff command. This output will show the differences between the two files or directories that you have specified. You can then use this output to determine which changes need to be made in order to bring the two files or directories in line with each other.
