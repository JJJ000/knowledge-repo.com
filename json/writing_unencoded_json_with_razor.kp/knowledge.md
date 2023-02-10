---
title: What is the process for displaying unencoded JSON in my view using razor?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the @Html.Raw() method to write unencoded JSON to the view using Razor.
---

**Contents**

[TOC]

## Section 1: Create a View Model

The first step in writing unencoded JSON to a View using Razor is to create a View Model. A View Model is an object that contains all of the data that will be passed to the View. This data can include any type of information that is necessary for the View to render the page, such as strings, numbers, boolean values, and even objects. 

## Section 2: Create a JSON String

Once the View Model has been created, the next step is to create a JSON string. This string can be created manually by writing out the JSON syntax, or it can be generated using a library such as Newtonsoft.JSON. The JSON string should contain all of the data that is contained in the View Model. 

## Section 3: Pass the JSON String to the View

Once the JSON string has been created, it can be passed to the View. This can be done by setting the View's Model property to the JSON string, or by passing the JSON string as an argument to the View's constructor. 

## Section 4: Render the JSON String

Finally, the JSON string can be rendered in the View by using the @Html.Raw() helper method. This method will render the JSON string as-is, without encoding it. This will ensure that the JSON string is displayed correctly in the View.
