---
title: Exclude all files of a certain type, except those located in a specific subfolder, from being tracked by git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a .gitignore file that ignores all files of a certain type, except those in a specific subfolder by adding an exception rule for the subfolder at the end of the file.
---

**Contents**

[TOC]

### Create .gitignore File
1. Create a `.gitignore` file in the root directory of your project.

### Add File Types to Ignore
2. Add the file types you want to ignore to the `.gitignore` file. For example, if you want to ignore all `.txt` files, add the following line to the `.gitignore` file:

```
*.txt
```

### Exclude Subfolder
3. To exclude a specific subfolder, add the following line to the `.gitignore` file, replacing `<subfolder>` with the name of the subfolder you want to exclude:

```
!<subfolder>/*.txt
```

### Commit Changes
4. Commit your changes to the `.gitignore` file.
