---
title: Ignore ^m when using 'git diff'
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Set the `core.whitespace` configuration option to `cr-at-eol` to make `git diff` ignore ^M.
---

**Contents**

[TOC]

1. Overview

Git diff is a command used to compare two different versions of a file. It will show the differences between the two versions, including any changes that have been made. Unfortunately, Git diff may also show ^M characters, which are created when files are transferred between Windows and Unix systems. This can be annoying and make the diff output difficult to read. Fortunately, there are ways to make Git diff ignore ^M characters. 

2. How to Make Git Diff Ignore ^M

The easiest way to make Git diff ignore ^M characters is to use the “--ignore-cr-at-eol” flag. This flag will tell Git to ignore any carriage returns (^M) at the end of lines. To use this flag, simply run the following command:

git diff --ignore-cr-at-eol

3. Other Options

If the “--ignore-cr-at-eol” flag does not work, there are other options available. One option is to use the “--ignore-space-at-eol” flag. This will tell Git to ignore any whitespace at the end of lines, including ^M characters. To use this flag, run the following command:

git diff --ignore-space-at-eol

Another option is to use the “--ignore-all-space” flag. This will tell Git to ignore all whitespace, including ^M characters. To use this flag, run the following command:

git diff --ignore-all-space

4. Conclusion

In conclusion, there are several ways to make Git diff ignore ^M characters. The easiest way is to use the “--ignore-cr-at-eol” flag, but there are other options available if this does not work. With these methods, you can make Git diff output easier to read and understand.
