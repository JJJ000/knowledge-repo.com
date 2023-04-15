---
title: Determine the number of lines in a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The number of lines in a git repository can be determined by running the `git ls-files` command.
---

**Contents**

[TOC]

1. Prerequisites
------------
- Git installed on your system

2. Counting Lines
------------
- Open a terminal window and navigate to the root folder of the git repository
- Execute the command `git ls-files | xargs wc -l`

3. Results
------------
The command will output the number of lines for each file in the repository, followed by the total number of lines for the repository.

4. Conclusion
------------
The command `git ls-files | xargs wc -l` can be used to quickly count the number of lines in a git repository.
