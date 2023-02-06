---
title: Using vimdiff to look at all the differences between "git diffs"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can view all git diffs with vimdiff by running the command `git difftool --tool=vimdiff`.
---

**Contents**

[TOC]

#### Setting up vimdiff
1. Install vimdiff: Vimdiff is included with the vim editor, so no additional installation is required.
2. Configure vimdiff: To configure vimdiff, open a terminal window and enter `git config --global diff.tool vimdiff`.

#### Viewing git diffs with vimdiff
1. Open a terminal window and enter `git diff` to compare two versions of a file.
2. Vimdiff will open in a split window, with the differences between the two files highlighted.
3. Use the navigation keys to move between the differences.
4. To accept changes from one version to the other, use the `do` command. To reject changes, use the `dp` command.
