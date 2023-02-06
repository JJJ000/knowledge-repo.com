---
title: It is impossible to overlook the presence of .idea/workspace.xml - it keeps appearing
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You should add .idea/workspace.xml to your .gitignore file.
---

**Contents**

[TOC]

# Ignoring File

To ignore the file, you will need to add the file path to your `.gitignore` file. This will tell Git to ignore the file when it is checked in.

# Adding File to .gitignore

To add the file to your `.gitignore` file, you will need to open the file and add the following line:

`/path/to/file/.idea/workspace.xml`

This will tell Git to ignore the file when it is checked in.

# Committing Changes

Once the file has been added to your `.gitignore` file, you will need to commit the changes to your repository. You can do this by running the following command:

`git commit -am "Added .idea/workspace.xml to .gitignore"`

# Pushing Changes

Finally, you will need to push the changes to your remote repository. You can do this by running the following command:

`git push origin master`
