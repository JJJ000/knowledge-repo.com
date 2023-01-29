---
title: How can I configure 'git diff' to show both line numbers and changed file names?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, you can use the `--name-only` and `--line-number` flags together to make `git diff` display the line numbers and changed file names.
---

**Contents**

[TOC]

`**` Setting Up**

1. Open your terminal and navigate to the directory containing the repository you'd like to view the changes of.

2. Run the command `git diff` to view the changes in the repository.

`**` Viewing Line Numbers**

1. To also view the line numbers of the changes, run the command `git diff --numstat`.

2. This will show the changes in the repository along with the number of lines added, deleted, and changed.

`**` Viewing File Names**

1. To view the file names of the changes, run the command `git diff --name-only`.

2. This will show the changes in the repository along with the file names of the changes.

`**` Combining Line Numbers and File Names**

1. To view the line numbers and file names of the changes, run the command `git diff --numstat --name-only`.

2. This will show the changes in the repository along with the line numbers and file names of the changes.
