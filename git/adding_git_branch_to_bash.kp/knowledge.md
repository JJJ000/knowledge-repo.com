---
title: Creating a git branch using the bash command line
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To add the current git branch to the Bash command prompt, use the command `export PS1=`\w \$(\_\_git\_ps1)``.
---

**Contents**

[TOC]

# Step 1: Install Git

In order to add the git branch to the Bash command prompt, you must first install git. You can do this by downloading the latest version of git from the official website and following the instructions given.

# Step 2: Setting Up Your Environment

Once you have installed git, you will need to set up your environment. This includes setting up your global user name and email address. You can do this by running the following commands:

```
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

# Step 3: Adding the Git Branch to the Bash Prompt

Once you have set up your environment, you can add the git branch to the Bash prompt. To do this, you will need to edit the Bash profile. You can do this by running the following command:

```
vi ~/.bash_profile
```

# Step 4: Adding the Git Branch

Once you have opened the Bash profile, you can add the git branch to the prompt. To do this, you will need to add the following line to the end of the file:

```
export PS1="\[\033[36m\]\u\[\033[m\]@\[\033[32m\]\h:\[\033[33;1m\]\w\[\033[m\]\$(__git_ps1) \$ "
```

Save the file and exit. You should now see the git branch on the Bash prompt.
