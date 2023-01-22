---
title: What happens if Jackson encounters an unrecognized field that is not marked to be ignored
authors:
- cool_wizard
tags:
- java
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-22 00:00:00
updated_at: 2023-01-22 00:00:00
tldr: If a field is not marked as ignorable, Jackson will throw an `UnrecognizedPropertyException`.
---

**Contents**

[TOC]

### What Is an Unrecognized Field?

An unrecognized field is a field in a JSON document that is not defined in the associated JSON schema. This type of field is not marked as ignorable, meaning that it is not ignored by the application processing the document.

### What Are the Consequences of Unrecognized Fields?

When an unrecognized field is encountered in a JSON document, it can cause a variety of issues, including:

• Data validation errors, as the field does not match what is expected.
• Security risks, as the field may contain malicious code.
• Performance issues, as the application must process the unrecognized field.

### How to Handle Unrecognized Fields?

There are several ways to handle unrecognized fields in a JSON document. These include:

• Ignoring the field: This can be done by marking the field as ignorable in the JSON schema.
• Logging the field: This can be done by adding a logging mechanism to the application to capture unrecognized fields and their values.
• Validating the field: This can be done by adding a validation mechanism to the application to ensure that the field is valid.

### Conclusion

Unrecognized fields in a JSON document can cause a variety of issues, including data validation errors, security risks, and performance issues. To mitigate these risks, it is important to handle unrecognized fields in a JSON document appropriately. This can be done by ignoring the field, logging the field, or validating the field.
