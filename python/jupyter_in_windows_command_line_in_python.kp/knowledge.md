---
title: How to execute jupyter on windows utilizing command line?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To start Jupyter from command line on Windows using Python, enter `jupyter notebook` in the command prompt or terminal.
---

**Contents**

[TOC]

Section 1: Installing Jupyter

Before you can run Jupyter, you need to install it on your Windows system. The easiest way to do this is by using pip, Python's package manager. Here are the steps:

1. Open Command Prompt or PowerShell.
2. Type `pip install jupyter` and press Enter.
3. Wait for the installation to complete. This may take a few minutes.

Section 2: Launching Jupyter

Once Jupyter is installed, you can launch it by running the jupyter-notebook command in Command Prompt or PowerShell. Here are the steps:

1. Open Command Prompt or PowerShell.
2. Navigate to the directory where you want to store your Jupyter notebooks. You can do this by typing `cd <path>` and pressing Enter, where <path> is the path to your desired directory.
3. Type `jupyter-notebook` and press Enter.
4. Wait for Jupyter to start, which may take a few seconds. A new browser window/tab should open automatically.

Section 3: Using Jupyter

Once Jupyter is running, you can create new notebooks or open existing ones. Here are the steps:

1. In the Jupyter interface, click New > Notebook > Python 3 (or another kernel you have installed).
2. A new notebook will open in a new tab. You can start writing code in the first cell.
3. To run a cell, click the Run button or press Shift + Enter. The output will appear below the cell.
4. To create a new cell, click the plus sign button or press Esc then A (to insert a cell above) or B (to insert a cell below).
5. To save your notebook, click File > Save or press Ctrl + S.

Section 4: Shutting Down Jupyter

Once you're done using Jupyter, you'll need to shut it down properly to avoid losing any unsaved work. Here are the steps:

1. In the Jupyter interface, click File > Close and Halt or press Ctrl + C in Command Prompt or PowerShell.
2. Wait for Jupyter to shut down completely. You'll see a message saying "Shutdown this Notebook Server (y/[n])?".
3. Type y and press Enter to confirm. Jupyter will shut down and you can now exit Command Prompt or PowerShell.
