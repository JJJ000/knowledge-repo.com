---
title: Displaying line numbers in ipython/jupyter notebooks
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To show line numbers in IPython/Jupyter Notebooks, click on `View` in the toolbar, then `Toggle Line Numbers`.
---

**Contents**

[TOC]

Introduction

IPython/Jupyter Notebooks are a great way to write and share interactive code, but they do not show line numbers by default. This can be a problem when trying to debug code or when trying to reference a specific line in a code cell.

In this article, we will explore different ways of showing line numbers in IPython/Jupyter Notebooks.

Using the command-line option

IPython/Jupyter Notebooks can be started with command-line options that modify their behavior. One such option is the `--IPythonApp.display_formatter_class` option, which can be used to specify a custom display formatter for IPython/Jupyter output.

To show line numbers in IPython/Jupyter Notebooks, we can start the Notebook with the following command:

```
jupyter notebook --NotebookApp.extra_static_paths=./custom --NotebookApp.webapp_settings={\"static_url_prefix\":\"/notebooks/custom/\"} --IPythonApp.display_formatter_class=notebook.services.config.CellDisplayFormatter --NotebookApp.token='' --NotebookApp.trust_xheaders=True --no-browser
```

This command starts a Jupyter Notebook with a custom static path and a custom display formatter that shows line numbers. The line numbers are displayed on the left side of each code cell.

Using a custom CSS file

Another way to show line numbers in IPython/Jupyter Notebooks is to use a custom CSS file. This method is more flexible than the command-line option, as it allows us to customize the appearance of the line numbers.

To use a custom CSS file, we first need to create a file called `custom.css` in the `profile_default/static/custom` directory of our IPython/Jupyter configuration directory. This directory is usually located in `~/.jupyter/` on Linux and macOS, and in `C:\Users\username\.jupyter\` on Windows.

Once we have created the `custom.css` file, we can add the following CSS rules to it:

```
div.CodeMirror-linenumber {
    display: inline-block;
    width: 20px;
    margin-right: 10px;
    color: #aaa;
}
```

These CSS rules make the line numbers be displayed on the left side of each code cell, just like in the previous method.

Using a Jupyter widget

A third way to show line numbers in IPython/Jupyter Notebooks is to use a Jupyter widget. Jupyter widgets are interactive HTML widgets that can display arbitrary content, such as line numbers.

To use a Jupyter widget to show line numbers, we first need to install the `jupyterlab-linenumber` package. This package adds a `LineNumber` widget that can be used to display line numbers in a Jupyter Notebook.

To install the `jupyterlab-linenumber` package, we can run the following command:

```
pip install jupyterlab-linenumber
```

Once we have installed the `jupyterlab-linenumber` package, we can add the following code to our Notebook to show line numbers:

```python
from jupyterlab_linenumber import LineNumber

ln = LineNumber(count_from=1)
ln.attach_to_cell()
```

This code creates a `LineNumber` widget and attaches it to each code cell in the Notebook. The `count_from` argument specifies the number of the first line (the default is 0).

Using an extension

Finally, we can also show line numbers in IPython/Jupyter Notebooks by using an extension. Extensions are JavaScript modules that can modify the behavior of IPython/Jupyter Notebooks.

One extension that can show line numbers in IPython/Jupyter Notebooks is the `jupyter_contrib_nbextensions` extension. This extension provides a `Line numbers` option that can be enabled in the Notebook interface.

To install the `jupyter_contrib_nbextensions` extension, we can run the following command:

```
pip install jupyter_contrib_nbextensions
```

Once we have installed the `jupyter_contrib_nbextensions` extension, we can enable the `Line numbers` option by running the following command:

```
jupyter nbextension enable --py --sys-prefix jupyter_contrib_nbextensions
```

Conclusion

In this article, we have explored different ways of showing line numbers in IPython/Jupyter Notebooks. We have seen how to use the command-line option, a custom CSS file, a Jupyter widget, and an extension to achieve this. Depending on our requirements and preferences, we can choose the method that suits us best.
