---
title: What is the best way to make an asmx file output json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Return an object or string in the ASMX file that is serialized to JSON.
---

**Contents**

[TOC]

## Section 1: Modify the Web.config File

1. Open the Web.config file in the root directory of your project.
2. Locate the <system.web.extensions> section and add the following code:

```
<scripting>
  <webServices>
    <jsonSerialization maxJsonLength="2147483644"/>
  </webServices>
</scripting>
```

## Section 2: Add the ScriptMethod Attribute

1. Open the ASMX file in the root directory of your project.
2. Locate the web method and add the following attribute:

```
[ScriptMethod(ResponseFormat = ResponseFormat.Json)]
```

## Section 3: Test the ASMX File

1. Compile and run the project.
2. Send a request to the ASMX file.
3. Check the response to ensure that it is in JSON format.

## Section 4: Troubleshooting

1. If the response is not in JSON format, check the Web.config file for any errors.
2. If the response is still not in JSON format, check the ScriptMethod attribute for any errors.
