---
title: How can I enable bash completion for aliases?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `complete -o default -o nospace -F \_git\_aliases <alias>` command to enable bash completion for aliases in Git.
---

**Contents**

[TOC]

# Section 1: Create an Alias

In order to use bash completion with Git aliases, you need to create an alias in your Git configuration. You can create an alias with the following command: 

`git config --global alias.aliasname 'command'`

For example, if you wanted to create an alias for the `git log` command, you could use the following command:

`git config --global alias.glog 'git log'`

# Section 2: Install Bash Completion

In order to use bash completion with your Git aliases, you need to install bash completion. Bash completion can be installed with the following command: 

`sudo apt-get install bash-completion`

# Section 3: Configure Bash Completion

Once you have installed bash completion, you need to configure it to recognize your Git aliases. This can be done by editing the `~/.bashrc` file and adding the following line: 

`complete -o default -o nospace -F _git glog`

This will tell bash completion to recognize the `glog` alias and provide completion options for it.

# Section 4: Activate Changes

Once you have configured bash completion for your Git aliases, you need to activate the changes by running the following command: 

`source ~/.bashrc`

This will activate the changes and allow you to use bash completion with your Git aliases.
