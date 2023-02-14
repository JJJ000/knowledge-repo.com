---
title: Include a virtual field in the JSON response
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: It is possible to add virtual attributes to a JSON output by using a custom serializer.
---

**Contents**

[TOC]

## Creating a Virtual Attribute

A virtual attribute is an attribute that is not stored in the database, but is instead generated from other attributes when needed. For example, a virtual attribute might calculate the age of a person based on their birthdate.

## Adding the Virtual Attribute to JSON Output

To add a virtual attribute to a JSON output, you must first define the attribute in the model. This is done using the `virtual` keyword. For example, to add an age attribute to a Person model, you would add the following code:

```
PersonSchema.virtual('age')
  .get(function() {
    return moment().diff(this.birthdate, 'years');
  });
```

Next, you must add the virtual attribute to the JSON output. This is done by adding the attribute name to the `toJSON` or `toObject` options. For example, to add the age attribute to the JSON output, you would add the following code:

```
PersonSchema.set('toJSON', {
  virtuals: true,
});
```

## Testing the Virtual Attribute

Once the virtual attribute has been added to the JSON output, you can test it by retrieving a document from the database and checking the JSON output. For example, if you have a Person document with a birthdate of January 1, 2000, the JSON output should include an age attribute with a value of 20.
