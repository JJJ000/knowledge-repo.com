---
title: How to use gson to specify optional and mandatory fields
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Optional fields in JSON are fields that can be omitted, while required fields must be included in the JSON.
---

**Contents**

[TOC]

## Optional Fields
Optional fields are those fields that can be omitted from a JSON object. These fields are not required to be included in the JSON object, and if they are not included, the parser will simply ignore them.

## Required Fields
Required fields are those fields that must be included in a JSON object. These fields are necessary for the parser to be able to properly interpret the object, and if they are not included, the parser will throw an error.
