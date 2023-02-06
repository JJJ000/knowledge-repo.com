---
title: What is the syntax for displaying a side-by-side comparison when using "git diff"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Include the `--side-by-side` flag when running the `git diff` command.
---

**Contents**

[TOC]

**Section 1: Install a diff Tool**

1. Install a diff tool such as Beyond Compare or Kdiff3.

**Section 2: Configure Git to Use the Diff Tool**

2. Configure Git to use the diff tool. This can be done by editing the .gitconfig file and adding the following lines:

```
[diff]
    tool = <diff tool name>
[difftool]
    prompt = false
[difftool "<diff tool name>"]
    cmd = <diff tool name> "$LOCAL" "$REMOTE"
```

**Section 3: Run the Diff Command**

3. Run the command `git difftool <commit1> <commit2>` to generate a side-by-side diff.

**Section 4: View the Diff**

4. The diff tool will open and show the side-by-side diff.
