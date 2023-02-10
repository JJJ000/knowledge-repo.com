---
title: Jackson changes the original boolean field by taking away the 'is'
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, the primitive boolean field can be renamed by removing the `is` prefix.
---

**Contents**

[TOC]

## Renaming

In JSON, primitive boolean fields can be renamed by removing the 'is' prefix. This is accomplished by simply replacing the 'is' prefix with an empty string. This will result in the field name being the same as the boolean value it represents.

## Syntax

The syntax for renaming a primitive boolean field in JSON is as follows:

```
{
    "fieldName": isValue
}
```

becomes

```
{
    "fieldName": Value
}
```

## Example

For example, if we have the following JSON object:

```
{
    "isActive": true
}
```

We can rename the field by removing the 'is' prefix:

```
{
    "active": true
}
```

## Benefits

By removing the 'is' prefix from primitive boolean fields in JSON, we can make the code more concise and easier to read. This also makes it easier to identify boolean fields, as they will no longer have the 'is' prefix.
