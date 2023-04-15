---
title: What is the correct procedure for shutting down ipython notebook?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Press Shift+L twice to log out and properly close the IPython Notebook.
---

**Contents**

[TOC]

# Steps to Close IPython Notebook

Here are the following steps to properly close IPython Notebook:

## Save and Checkpoint

Before closing the IPython Notebook, it is essential to save any unsaved work and create a checkpoint. A checkpoint is a saved version of the notebook at a particular point in time.

To save the Notebook, either click on the "Save" icon in the toolbar or press "Ctrl + S" on Windows or "Cmd + S" on Mac.

To create a checkpoint, click on "File" on the menu bar and select "Save and Checkpoint."

## Shutdown the IPython Notebook Server

After creating a checkpoint, it is essential to shut down the IPython Notebook server safely. This ensures that all the open files are properly closed and any running computation is completed.

To shut down the IPython Notebook server, switch to the Terminal/CMD and type `Ctrl+C`. Doing so will terminate the server and display a message that will confirm the server shutdown.

## Close the IPython Notebook Tab

After shutting down the IPython Notebook server, the final step is to close the Notebook tab on the web browser. Not closing the Notebook tab may cause problems if the server is running again.

To close the IPython Notebook tab, click on the "x" on the right-hand side of the tab or press "Ctrl + W" on Windows or "Cmd + W" on Mac.

## Closing the Web Browser

Once the IPython Notebook tab has been closed, the final step is to close the web browser that was used to access the Notebook. 

To close the web browser, either click on the "x" on the right-hand side of the tab or press "Ctrl + W" on Windows or "Cmd + W" on Mac.

The above steps help ensure that the IPython Notebook is properly closed, and there are no running processes left behind that may cause issues in the future use of the Notebook.
