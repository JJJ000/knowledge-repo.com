---
title: What is the best way to pass JSON as a parameter to an mvc 5 action method?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: A JSON object can be passed as a parameter to an MVC 5 action method by using the [FromBody] attribute.
---

**Contents**

[TOC]

**Section 1: Create a Model for the JSON**

The first step for receiving JSON as an MVC 5 action method parameter is to create a model that represents the JSON. This model should include all the properties that the JSON contains. For example, if the JSON contains a name, an age, and a list of hobbies, the model should include properties for each of these.

**Section 2: Create an Action Method**

The next step is to create an action method that will accept the JSON as a parameter. This action method should include the model as a parameter, and should specify that the parameter should be passed in as JSON.

**Section 3: Deserialize the JSON**

Once the action method has been created, the JSON must be deserialized into the model. This can be done using the Newtonsoft.Json library. This library will take the JSON string and deserialize it into the model.

**Section 4: Use the Model**

Once the JSON has been deserialized, the model can be used by the action method. The action method can then use the properties in the model to perform the desired tasks.
