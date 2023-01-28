---
title: Can git-reflog be configured to display a date with each entry?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, you can use the `--date=relative` option to show a relative date alongside each entry.
---

**Contents**

[TOC]

`**` Overview**

Git-reflog is a command-line tool used to view the local repository's history of changes. It is used to view, navigate, and recover older commits. By default, git-reflog does not show dates alongside each entry.

`**` Adding Dates to git-reflog Output**

Fortunately, it is possible to add dates to the git-reflog output. This can be done by using the --date=short flag when running the git-reflog command. Adding this flag will cause the output to include a date in the format YYYY-MM-DD alongside each entry.

`**` Example Usage**

For example, if you wanted to view the git-reflog for the current repository and add dates to the output, you could run the following command:

```git
git reflog --date=short
```

`**` Further Reading**

For more information about git-reflog, refer to the official documentation: 
https://git-scm.com/docs/git-reflog
