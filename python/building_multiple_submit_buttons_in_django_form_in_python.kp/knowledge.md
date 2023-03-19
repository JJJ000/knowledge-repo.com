---
title: What is the approach to create numerous submit buttons in a django form?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use Django`s form and template system to create multiple forms with different action URLs and submit buttons.
---

**Contents**

[TOC]

## Creating Multiple Submit Buttons in Django Forms

Django is an open-source framework that facilitates the development of complex and data-driven web applications. When building web apps, you might need to have multiple submit buttons in your Django form for different functionalities or actions. Here are the steps to create multiple submit buttons in a Django form:

### 1. Create a Django Form

To create a Django form, you'll need to create a new file. This file will define the form and its fields. Once you have created the file, you'll need to import the necessary functions and modules. You will also define the form fields, which could include fields such as text fields, radio buttons, checkboxes, and dropdown lists. 

### 2. Define the Submit Buttons 

Once you have defined your form fields, you'll need to add the submit buttons to the form. You can do this by creating a button element and use Django's HTML helper to create the button. The helper function sets the value and the name attribute of the submit button.

### 3. Handle the Submit Button Actions

Since you will have multiple submit buttons in your Django form, you'll need to handle their actions. To handle the actions, you'll define the view function to be executed when the submit button is clicked. The view function will check which submit button was clicked and execute its corresponding function. The functions can include validation of the form, form processing, and database query, among others.

### 4. Render the Form

After defining the submit button actions, you'll need to render the form with the submit buttons on your webpage. You can use Django's template engine to render the form on the webpage. To render the form, you'll create a template file that will display the form's fields and the submit buttons. When the user clicks a submit button, Django will execute the appropriate view function based on the submit button's name.

With these four steps, you can easily create a Django form with multiple submit buttons. It provides a user-friendly interface for the website visitors and saves the website developer lots of time.
