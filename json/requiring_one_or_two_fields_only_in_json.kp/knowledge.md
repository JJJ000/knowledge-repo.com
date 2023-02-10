---
title: Which of the three fields do I need to include, and which can I leave out?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can require one field or another using the `required` keyword in the JSON schema.
---

**Contents**

[TOC]

1. **Using Conditional Validation**

Conditional validation allows you to require one field or another depending on the value of another field. To do this, you need to define a validation schema that contains the fields you want to validate and the rules that should be applied to each field. In the validation schema, you can specify which fields are required depending on the value of another field.

For example, if you want to require either field A or field B, but not both, you can define a validation schema with the following rules:

- Field A is required if field B is not present
- Field B is required if field A is not present

2. **Using Nested Objects**

Another way to require one field or another is to use nested objects. In this approach, you can define an object that contains both fields and then set a validation rule on the object, requiring one of the fields to be present.

For example, if you want to require either field A or field B, but not both, you can define an object with the following structure:

```
{
  fieldA: {
    type: String
  },
  fieldB: {
    type: String
  }
}
```

Then you can set a validation rule on the object, requiring one of the fields to be present:

```
{
  type: Object,
  required: {
    oneOf: [
      {
        fieldA: {
          type: String
        }
      },
      {
        fieldB: {
          type: String
        }
      }
    ]
  }
}
```

3. **Using a Custom Validator**

If you need more flexibility or control over the validation logic, you can create a custom validator. In this approach, you can define a function that takes the JSON data as an argument and then performs the validation logic you need.

For example, if you want to require either field A or field B, but not both, you can create a function that checks if either field is present and returns an error if both are present:

```
const validateFields = (data) => {
  if (data.fieldA && data.fieldB) {
    return new Error('Either field A or field B must be present, but not both.');
  }
  return true;
};
```

Then you can use this function in your validation schema:

```
{
  type: Object,
  validator: validateFields
}
```

4. **Using a Custom Validation Library**

Finally, if you need more complex validation logic, you can use a custom validation library. Many libraries provide a wide range of validation rules and functions that can be used to create complex validation logic.

For example, if you want to require either field A or field B, but not both, you can use the `oneOf` validation rule from the [validator.js](https://github.com/chriso/validator.js) library:

```
{
  type: Object,
  validator: validator.oneOf([
    {
      fieldA: {
        type: String
      }
    },
    {
      fieldB: {
        type: String
      }
    }
  ])
}
```
