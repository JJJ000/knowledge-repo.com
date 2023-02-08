---
title: Use jq to choose objects based on the value of a given variable in the object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: jq can be used to select objects based on the value of a variable within the object by using the `.variable\_name` syntax.
---

**Contents**

[TOC]

**Section 1: What is jq?**

jq is a command-line JSON processor. It allows users to parse and filter JSON data, as well as transform it into new formats. It is an open source tool written in C and released under the MIT license.

**Section 2: How to Select Objects Based on Value of Variable in Object**

To select objects based on the value of a variable in the object, you can use the `.` operator to access the value of the variable and then use the `==` operator to compare it to the desired value. For example, if you have a JSON object that contains an array of objects and you want to select the objects with a certain value for the variable "status", you could use the following command:

```
jq '.[] | select(.status == "active")'
```

**Section 3: Example**

Let's say we have the following JSON object:

```
{
  "users": [
    {
      "name": "John",
      "status": "active"
    },
    {
      "name": "Jane",
      "status": "inactive"
    },
    {
      "name": "Bob",
      "status": "active"
    }
  ]
}
```

To select the objects with a status of "active", we could use the following command:

```
jq '.users[] | select(.status == "active")'
```

This command would return the following result:

```
[
  {
    "name": "John",
    "status": "active"
  },
  {
    "name": "Bob",
    "status": "active"
  }
]
```

**Section 4: Conclusion**

jq is a powerful command-line JSON processor that allows users to select objects based on the value of a variable in the object. By using the `.` operator to access the value of the variable, and the `==` operator to compare it to the desired value, users can easily select the desired objects.
