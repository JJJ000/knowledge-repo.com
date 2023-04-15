---
title: Is it possible to specify an unlimited value for maxJSONlength in web.config?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, set the `maxJsonLength` attribute to its maximum allowed value of `2,147,483,647`
---

**Contents**

[TOC]

### Maximum Allowed Value for maxJsonLength

It is possible to set an unlimited length for maxJsonLength in web.config. This can be achieved by setting the maxJsonLength attribute to its maximum allowed value of `2,147,483,647`.

### Steps

1. Open the web.config file of the application.
2. Add the following code inside the <configuration> element:

```xml
<system.web.extensions>
  <scripting>
    <webServices>
      <jsonSerialization maxJsonLength="2147483647"/>
    </webServices>
  </scripting>
</system.web.extensions>
```

3. Save the changes and restart the application.

### Benefits

Setting an unlimited length for maxJsonLength in web.config can help to improve the performance of web applications. This is because it allows the application to process large amounts of data without causing any issues. Additionally, it can help to reduce the amount of time it takes for the application to respond to requests.
