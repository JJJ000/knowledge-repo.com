---
title: What is the simplest method for creating a cascading dropdown menu in ASP.NET mvc 3 using c#?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: The easiest way to create a cascade dropdown in ASP.NET MVC 3 with C# in Json is to use the JsonResult action method.
---

**Contents**

[TOC]

1. **Create a Controller Action Method**

Create a controller action method that will return the Json data for the cascade dropdown. The method should accept the id of the parent item and return the Json data for the child items.

2. **Create a View Model**

Create a view model that will contain the data for the cascade dropdown. The view model should contain the parent item id and a list of child items.

3. **Create the Json Data**

Create the Json data for the cascade dropdown by looping through the list of child items in the view model and adding them to the Json object.

4. **Render the Json Data**

Render the Json data in the controller action method by returning the Json object. The controller action method should return the Json data as an ActionResult.
