---
title: What is the process for uploading, modifying, executing, and saving text files in the form of .py format to an ipython notebook cell?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To load/edit/run/save text files (.py) into an IPython notebook cell, use the %load, %edit, %run, and %%writefile magic commands.
---

**Contents**

[TOC]

1. Loading a Text File into an IPython Notebook Cell:
-----------------------------------------------------

To load a python file (.py) into an IPython notebook cell, we can make use of the 'magic command' feature of IPython. The magic command %load takes a file name as its argument and pastes the contents of that file into the cell. The steps are as follows:

    a) Open an empty IPython notebook cell.
    
    b) Type the code '%load filename.py' (without quotes).
    
    c) Replace the 'filename.py' with the actual name of the file that you want to load into the cell.
    
    d) Run the cell (shift+enter).
    
    e) IPython will load the contents of the file into the cell.


2. Editing the Text File in the IPython Notebook Cell:
------------------------------------------------------

Once the text file is loaded into the cell, we can edit the file using the IPython notebook's cell editor. The steps are as follows:

    a) Click on the IPython cell that contains the text file.
    
    b) Edit the contents of the cell as per your requirement.
    
    c) Once the editing is done, run the cell (shift+enter) to save the changes.
    
    d) If you want to revert back to the original file contents, you can simply load the file again using the '%load filename.py' command.


3. Running the Text File in the IPython Notebook Cell:
-----------------------------------------------------

After loading and editing the text file, we can run the file contents directly from the IPython notebook cell without having to save it separately. The steps are as follows:

    a) Ensure that the code in the cell is valid python code and that there are no syntax errors.
    
    b) Click on the IPython cell that contains the python code.
    
    c) Run the cell (shift+enter) to execute the code.
    
    d) The output, if any, will be displayed below the cell.


4. Saving the Text File from the IPython Notebook Cell:
------------------------------------------------------

After loading and editing the text file, if you wish to save the changes back to the original file, you can use the %writefile magic command. It saves the contents of the cell back to the specified file. The steps are as follows:

    a) Click on the IPython cell that contains the edited file contents.
    
    b) Type the code '%writefile filename.py' (without quotes).
    
    c) Replace the 'filename.py' with the actual name of the file that you want to save the edited contents to.
    
    d) Run the cell (shift+enter).
    
    e) IPython will save the edited file contents back to the specified file, overwriting the existing file.
