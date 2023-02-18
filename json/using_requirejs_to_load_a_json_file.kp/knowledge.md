---
title: What is the procedure for loading a static JSON file using requirejs?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Use the require.js text! plugin to load the static JSON file.
---

**Contents**

[TOC]

1. Set up the RequireJS Configuration 

Before you can start loading JSON files with RequireJS, you need to set up the configuration. This is done by creating a require.config() object and adding any specific configuration options you need. For example, if you are loading a JSON file from a different domain, you can set the paths option to the URL of the file.

2. Load the JSON File 

Once the configuration is set up, you can use the require() function to load the JSON file. This is done by passing a single argument to the function, which is the path to the JSON file. This path can be either relative to the current page or an absolute URL.

3. Access the JSON Data 

Once the JSON file is loaded, you can access the data contained within it. This is done by passing a callback function to the require() function. This callback function is then executed when the file is loaded, and the data is passed to the function as an argument.

4. Use the JSON Data 

Finally, you can use the data contained within the JSON file. This is done by accessing the data within the callback function. The data is usually stored in an object, so you can access it by using dot notation or bracket notation. Once you have access to the data, you can use it however you need.
