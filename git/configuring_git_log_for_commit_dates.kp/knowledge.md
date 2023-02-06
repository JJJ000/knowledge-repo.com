---
title: What settings do I need to change to make 'git log' display the commit date?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git log --pretty=format`%cd` --date=local` to show the commit date in the local timezone.
---

**Contents**

[TOC]

# Section 1 - Configure Log Format

To configure the 'git log' command to show the commit date, you will need to first configure the log format. This can be done by running the following command:

`git config --global log.date "%cD"`

This will configure the log format to include the commit date in the output.

# Section 2 - Run Log Command

Once the log format has been configured, you can then run the 'git log' command to view the commit date for each commit. The command syntax is as follows:

`git log --pretty=format:"%h %cD"`

# Section 3 - View Output

Once the 'git log' command has been run, the output will include the commit date for each commit. This will be displayed in the following format:

`<commit hash> <commit date>`

# Section 4 - Example Output

For example, the output of the 'git log' command may look something like this:

`8cef0a2 Fri May 15 17:34:23 2020`
