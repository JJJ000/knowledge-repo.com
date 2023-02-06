---
title: Viewing the history of a single revision in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To view the log of a single revision, use the git log command with the revision`s hash as an argument.
---

**Contents**

[TOC]

# Section 1: Git Log Syntax

The syntax for viewing the log of a single revision is:

`git log -1 <revision>`

Where `<revision>` is the desired revision number.

# Section 2: Output

The output of the git log command for a single revision will include the following information:

* Commit hash
* Author
* Date
* Commit message

# Section 3: Options

The `git log` command has a number of options that can be used to customize the output. These include:

* `--pretty` to format the output
* `--stat` to show a summary of the changes
* `--patch` to show the changes made in the commit
* `--name-only` to show the names of the files changed

# Section 4: Example

For example, to view the log of revision `12345`, the command would be:

`git log -1 12345`
