---
title: It is not possible to display a git tree in the command line
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git does not have a built-in command for showing a tree in the terminal.
---

**Contents**

[TOC]

### Using a GUI

One way to view the Git tree in a terminal is to use a graphical user interface (GUI). This is a visual way to view the tree, and it can be done in several different ways.

For example, you can use a dedicated Git GUI such as GitKraken or SourceTree, which will show the tree in a graphical format. You can also use a text editor such as Sublime Text or Atom, which have plugins that can display the tree in a graphical way.

### Using the Command Line

Another way to view the Git tree in a terminal is to use the command line. This is a more technical approach, but it can be done with a few simple commands.

The first command you need to use is `git log --graph --oneline --decorate`. This will show the tree in a linear format, with each commit represented by a single line.

You can also use the `git log --graph --all --decorate` command, which will show the tree in a more graphical way. This command will show the commits in a tree-like format, with branches and merges represented by branches and arrows.

### Using External Tools

Finally, there are a few external tools that can be used to view the Git tree in a terminal. These tools include tig, which is a text-based interface for viewing the tree, and git-tree, which is a command line tool for visualizing the tree.

These tools can be used to view the tree in a more graphical way, and they can be used to explore the history of the project in more detail.
