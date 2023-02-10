---
title: What is the best way to save a basic settings/config file using python?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Save the settings/config file as a .json file.
---

**Contents**

[TOC]

1. **Creating the Json File**
  - Create a text file with the .json extension
  - Open the file with a text editor and add the settings/config you would like to save
  - Enclose the settings/config in curly braces {}

2. **Formatting the Json File**
  - Format the settings/config in a key-value pair format, where each setting has a name and a value
  - Separate each key-value pair with a comma
  - If the value of a setting is a list or an object, enclose it in square brackets [] or curly braces {}

3. **Saving the Json File**
  - Save the file with the same name and extension

4. **Loading the Json File**
  - Use the json.load() method in Python to load the file
  - Pass the file path of the json file as an argument to the json.load() method
  - Access the settings/config from the loaded json file using the keys
