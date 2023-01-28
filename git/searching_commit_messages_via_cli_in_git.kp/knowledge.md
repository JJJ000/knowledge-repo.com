---
title: What is the command to search commit messages from the command line?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To search in commit messages using command line in Git, use the `git log` command with the `--grep` flag.
---

**Contents**

[TOC]

### Section 1 - Formatting the Search

The basic command for searching commit messages in Git is `git log`. This command can be modified with various flags to specify the search criteria.

For example, to search for a specific word in commit messages, the `--grep` flag can be used, followed by the word to be searched.

`git log --grep="<word>"`

### Section 2 - Refining the Search

The `--author` flag can be used to refine the search to a specific author.

`git log --grep="<word>" --author="<author>"`

The `--since` and `--until` flags can be used to limit the search to a specific date range.

`git log --grep="<word>" --author="<author>" --since="<date>" --until="<date>"`

### Section 3 - Output Formatting

The `--oneline` flag can be used to format the output in a single line for each commit.

`git log --grep="<word>" --author="<author>" --since="<date>" --until="<date>" --oneline`

### Section 4 - Viewing the Search Results

The `--no-merges` flag can be used to exclude merge commits from the results.

`git log --grep="<word>" --author="<author>" --since="<date>" --until="<date>" --oneline --no-merges`

This command will output a list of commits with their message, author and date. The list can be viewed in the terminal or piped to a file for further analysis.
