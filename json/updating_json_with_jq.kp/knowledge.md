---
title: What is the syntax for updating a single value in a JSON document using jq?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the `set` command to update a single value in a JSON document using jq.
---

**Contents**

[TOC]

#### Step 1: Get the Desired Value

Using jq, the desired value can be accessed using the dot notation. For example, to get the value of the key `name` from a JSON document, the following command can be used:

```
jq '.name' <document.json>
```

This will return the value of the `name` key from the document.

#### Step 2: Update the Value

Once the desired value has been accessed, it can be updated using the `set` command. For example, to update the value of the key `name` to `John`, the following command can be used:

```
jq 'set(.name, "John")' <document.json>
```

This will update the value of the `name` key to `John`.

#### Step 3: Output the Document

Finally, the updated JSON document can be output using the `--output` flag. For example, to output the updated document to a file called `updated_document.json`, the following command can be used:

```
jq --output updated_document.json 'set(.name, "John")' <document.json>
```

This will output the updated JSON document to the specified file.
