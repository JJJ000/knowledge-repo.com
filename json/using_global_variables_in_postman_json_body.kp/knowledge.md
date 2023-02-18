---
title: How can a global variable be included in a JSON body using postman?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Global variables can be passed into a JSON body by using the double curly braces syntax {{variableName}}.
---

**Contents**

[TOC]

## Setting the Global Variable 

The first step is to set the global variable. This can be done by selecting the "Globals" tab in the top right corner of the Postman UI. 

Once the Globals tab is selected, the user can then click the "Add" button to create a new variable. The user can then enter the variable name, value, and type. 

## Passing the Global Variable into the JSON Body 

The next step is to pass the global variable into the JSON body. This can be done by using the `{{variable_name}}` syntax in the body. 

For example, if the global variable is named `my_variable` and has a value of `foo`, the user can pass the variable into the JSON body by using the syntax `{{my_variable}}`. 

## Testing the Request 

Once the global variable is set and the syntax is used in the JSON body, the user can then test the request by sending it. If the request is successful, the response will contain the value of the global variable. 

## Debugging the Request 

If the request fails, the user can use the Postman console to debug the request. The Postman console will show any errors that occurred and provide helpful information on how to fix them.
