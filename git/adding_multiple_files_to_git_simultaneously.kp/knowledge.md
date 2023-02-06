---
title: How can I commit multiple files to git simultaneously?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the command `git add <file1> <file2> <file3> ...` to add multiple files to Git at the same time.
---

**Contents**

[TOC]

#1 Using Wildcards

One way to add multiple files to Git at the same time is by using wildcards. Wildcards are symbols that can be used to represent one or more characters in a file name. They are used to create a pattern that can be used to match multiple files. 

For example, if you wanted to add all the files with the extension ".txt" in the current directory to Git, you could use the command: 

`git add *.txt`

#2 Using a List of Files

Another way to add multiple files to Git at the same time is by using a list of files. This can be done by using the command `git add` followed by a list of the files you want to add. 

For example, if you wanted to add the files "file1.txt", "file2.txt" and "file3.txt" to Git, you could use the command: 

`git add file1.txt file2.txt file3.txt`

#3 Using a Script

A third way to add multiple files to Git at the same time is by using a script. This can be done by writing a script that will loop through all the files in a directory and add them to Git one by one. 

For example, if you wanted to add all the files in the current directory to Git, you could use a script like this: 

```
#!/bin/bash
for file in *
do
    git add $file
done
```

#4 Using a GUI

Finally, you can also add multiple files to Git at the same time using a graphical user interface (GUI). Most popular Git clients, such as GitHub Desktop, provide an easy way to select multiple files and add them to Git with a single click.
