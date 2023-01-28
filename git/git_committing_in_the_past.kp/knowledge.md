---
title: What is the process for creating a git commit from a previous time period?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the `git commit --date` option to make a Git commit in the past.
---

**Contents**

[TOC]

### Create a New Commit

The first step is to create a new commit with the desired timestamp. To do this, you will need to use the `git commit --date` command. This command allows you to specify a custom timestamp for the commit. 

### Formatting the Date

When specifying the date, you will need to use a specific format. The format should be `YYYY-MM-DDTHH:MM:SS+00:00` where `YYYY` is the year, `MM` is the month, `DD` is the day, `HH` is the hour, `MM` is the minute, and `SS` is the second. 

### Example

For example, if you wanted to make a commit with the timestamp of January 1st, 2020 at 12:00pm, you would use the command `git commit --date="2020-01-01T12:00:00+00:00"`.

### Finalizing the Commit

Once the command is executed, you will be prompted to enter a commit message. After entering the commit message, the commit will be finalized and the timestamp will be set to the specified date.
