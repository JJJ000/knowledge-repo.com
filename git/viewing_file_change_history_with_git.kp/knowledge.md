---
title: How to examine the past modifications of a file using git tracking?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To view the change history of a file using Git versioning, use the command `git log <file name>`.
---

**Contents**

[TOC]

### Viewing File History

To view the change history of a file using Git versioning, you can use the `git log` command. This command will display a list of commits that have been made to the file, along with the date, author, and commit message associated with each commit.

### Filtering Results

You can also use the `git log` command to filter the results. For example, you can use the `--follow` flag to show only commits that affected a specific file, or you can use the `--author` flag to show only commits made by a specific author.

### Viewing Differences

In addition to viewing the history of a file, you can also view the differences between different versions of the file. To do this, you can use the `git diff` command. This command will show you the differences between the current version of the file and the version from a previous commit.

### Other Options

Finally, you can also use the `git blame` command to view the history of a file. This command will show you the author, date, and commit message associated with each line of the file. This can be useful for tracking down bugs or understanding how a particular piece of code was written.
