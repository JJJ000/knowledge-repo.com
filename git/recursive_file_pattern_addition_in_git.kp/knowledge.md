---
title: Add files using a recursive pattern
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git can recursively add files by pattern using the `git add -A <pattern>` command.
---

**Contents**

[TOC]

# Section 1: Using Git Add

Git Add is the primary command used to add files to the staging area. This command can be used to add files recursively by pattern. To do this, simply use the -A (all) flag. This flag will add all files, including those in subdirectories, to the staging area.

For example, to add all files with the .txt extension, you can use the following command:

```
git add -A *.txt
```

# Section 2: Using Git Add with Pathspec

Git Add can also be used with the --pathspec flag. This flag allows you to specify a particular pattern or path to add files from. For example, to add all files in the "docs" directory with the .txt extension, you can use the following command:

```
git add --pathspec docs/*.txt
```

# Section 3: Using Git Add with Multiple Patterns

Git Add can also be used with multiple patterns. This can be done by simply separating the patterns with a comma. For example, to add all files in the "docs" directory and all files with the .txt extension, you can use the following command:

```
git add -A docs/*, *.txt
```

# Section 4: Using Git Add with Wildcards

Git Add can also be used with wildcards. This allows you to add files with a certain pattern, regardless of the directory they are in. For example, to add all files with the .txt extension, you can use the following command:

```
git add -A *txt
```
