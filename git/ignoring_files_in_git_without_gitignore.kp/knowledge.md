---
title: What is the alternative method to using .gitignore to make git ignore files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can make Git ignore files by adding a pathspec to the .git/info/exclude file.
---

**Contents**

[TOC]

1. Create a Global Exclude File 

Using a global exclude file, you can create a file that will be used to ignore files from all of your Git repositories. The global exclude file is usually located in the user’s home directory, and is named .gitignore_global. To create the global exclude file, create a text file and add the patterns for the files you want to ignore. 

2. Configure Git to Use the Global Exclude File 

Once the global exclude file is created, you need to configure Git to use it. To do this, you need to set the core.excludesfile configuration variable in the global Git configuration file. The global configuration file is usually located in the user’s home directory, and is named .gitconfig. To set the core.excludesfile configuration variable, add the following line to the configuration file: 

`core.excludesfile = ~/.gitignore_global`

3. Add Patterns to the Global Exclude File 

Once the global exclude file is configured, you need to add the patterns for the files you want to ignore. The patterns should be added one per line, and should be relative to the root of the repository. For example, if you want to ignore all files with the .tmp extension, you can add the following line to the global exclude file: 

`*.tmp`

4. Commit the Global Exclude File 

Finally, you need to commit the global exclude file. This will ensure that the changes are applied to all of your repositories. To commit the global exclude file, use the following command: 

`git add .gitignore_global`

`git commit -m "Added global exclude file"`
