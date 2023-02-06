---
title: Setting up a comparison tool using the .gitconfig file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Configure the diff tool in the [diff] section of the .gitconfig file.
---

**Contents**

[TOC]

#### Section 1: Install Diff Tool

Before you can use a diff tool with your `.gitconfig` file, you must first install the diff tool you want to use. Popular diff tools include `KDiff3`, `Meld`, `DiffMerge`, and `WinMerge`. 

#### Section 2: Configure `.gitconfig`

Once you have installed the diff tool of your choice, you can configure `.gitconfig` to use it. Open the `.gitconfig` file, located in the `~/.git` directory, and add the following lines:

```
[diff]
    tool = <tool name>
[difftool]
    prompt = false
[difftool "<tool name>"]
    cmd = <path to diff tool executable> "$LOCAL" "$REMOTE"
```

Replace `<tool name>` with the name of the diff tool you installed, and `<path to diff tool executable>` with the path to the diff tool executable file.

#### Section 3: Use Diff Tool

Once your `.gitconfig` file is configured, you can use the diff tool with the following command:

```
$ git difftool <commit>
```

Replace `<commit>` with the commit you want to compare.

#### Section 4: Troubleshooting

If you encounter any issues while configuring or using the diff tool, make sure that the path to the diff tool executable is correct and that the `.gitconfig` file is properly configured. If the problem persists, try reinstalling the diff tool.
