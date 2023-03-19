---
title: What are the steps to include a conda environment in jupyter lab?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: `Run the command `conda activate <environment\_name>` in your Jupyter Lab terminal, then install the `ipykernel` package using `conda install ipykernel` to add the environment to Jupyter Lab.`
---

**Contents**

[TOC]

# Adding Conda environment to Jupyter Lab in Python

Jupyter Lab is a versatile tool that allows users to execute and test their code in a streamlined and user-friendly way. One of the benefits of using Jupyter Lab is the ability to create and switch between different virtual environments or conda environments. In this tutorial, we’ll explore the steps to add a conda environment to Jupyter Lab.

## Section 1: Creating a Conda environment

The first step is creating a conda environment. If you already have an environment that you want to use, skip this section. To create a new conda environment, open your terminal or Anaconda Prompt (if using Windows) and run the following command:

```
conda create --name myenv
```

Here, "myenv" is the name of your new conda environment. You can choose any name you like. Once you run this command, conda will create a new environment with the default packages.

## Section 2: Activating and installing packages in the Conda environment

Next, activate the conda environment by running the following command:

```
conda activate myenv
```

Here, "myenv" is the name of your conda environment. Once the conda environment is activated, you can install any packages you need using the conda install command. For example, to install numpy and pandas, you can run the following command:

```
conda install numpy pandas
```

## Section 3: Installing the Jupyter Lab kernel

The next step is to install the Jupyter Lab kernel for the conda environment. This will allow Jupyter to recognize the packages in the conda environment. To install the kernel, run the following command:

```
python -m ipykernel install --user --name myenv --display-name "My Environment"
```

Here, “myenv” is the name of your conda environment and “My Environment” is the display name for the kernel. Once you run this command, the kernel is installed and ready to use in Jupyter Lab.

## Section 4: Launching Jupyter Lab and switching to the conda environment

Finally, launch Jupyter Lab in your browser by running the following command:

```
jupyter lab
```

Once Jupyter Lab opens in the browser, you can create a new notebook or open an existing one. To switch to the conda environment, click on the “Kernel” dropdown menu and select “Change kernel”. You should see the name of the conda environment you just created (“My Environment” in our example). Select it, and you can now run codes using the packages installed in the conda environment.

In conclusion, adding a conda environment to Jupyter Lab is a straightforward process. By following these steps, you can create a virtual environment, install packages, and switch to the environment within Jupyter Lab. This allows you to organize your code and dependencies and ensure that your code runs in the correct environment. Happy coding!
