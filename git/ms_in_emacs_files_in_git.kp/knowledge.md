---
title: What is the meaning of the ^m symbols appearing in my files when I open them in emacs?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The ^M`s are carriage return characters that are caused by Windows line endings.
---

**Contents**

[TOC]

1. What is a ^M?
----------------
A ^M is a carriage return character (CR) that is used to signify the end of a line in a file. It is represented in Emacs as a control character, which is denoted by the caret (^) and the letter M.

2. How Does it Show Up in Files?
-------------------------------
The ^M character can show up in files when the file is edited on a system that uses a different line ending than the one the file was created on. For example, if a file is created on a Windows system that uses the CR+LF line ending (carriage return + line feed) and then edited on a Unix system that uses the LF line ending, the ^M character will appear in the file.

3. How Does it Show Up in Git?
------------------------------
When a file is committed to a Git repository, the ^M character may appear in the output of the `git diff` command. This is because the CR+LF line endings used by Windows systems are not compatible with the LF line endings used by Unix systems, so the ^M character is used to indicate the difference between the two.

4. How Can it Be Fixed?
------------------------
The ^M character can be removed from files by using the `dos2unix` command. This command will convert all CR+LF line endings to LF line endings, which will remove the ^M character from the file.
