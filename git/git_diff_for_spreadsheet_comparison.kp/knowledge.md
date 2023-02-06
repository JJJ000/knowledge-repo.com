---
title: What is the best way to generate a comprehensible comparison of two spreadsheets with git diff?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the command `git diff <file1> <file2>` to create a readable diff of two spreadsheets.
---

**Contents**

[TOC]

## Step 1: Export Spreadsheets as Text Files

In order to use `git diff` to compare two spreadsheets, they must first be exported as text files. This can be done in a variety of ways, depending on the type of spreadsheet you are using. For example, if you are using Microsoft Excel, you can save the file as a CSV (Comma Separated Values) file.

## Step 2: Add Text Files to Git Repository

Once the spreadsheets have been exported as text files, they can be added to a Git repository. This can be done by using the `git add` command.

## Step 3: Use Git Diff to Compare Text Files

Once the text files have been added to the Git repository, you can use the `git diff` command to compare them. This will generate a readable diff of the two spreadsheets, showing any differences between them.

## Step 4: View Diff Output

The output of the `git diff` command can be viewed in a variety of ways. For example, you can use a text editor to view the output, or you can use a graphical diff tool such as Meld or KDiff3.
