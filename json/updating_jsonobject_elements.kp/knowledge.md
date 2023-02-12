---
title: Modify items in a jsonobject
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the put() method to update elements in a JSONObject.
---

**Contents**

[TOC]

**Section 1: Retrieve the JSONObject**

The first step is to retrieve the JSONObject that needs to be updated. This can be done using the `getJSONObject()` method. The syntax for this method is as follows:

`JSONObject jsonObject = jsonObject.getJSONObject(String key);`

where `key` is the name of the JSONObject that needs to be retrieved.

**Section 2: Update the JSONObject**

Once the JSONObject is retrieved, it can be updated using the `put()` method. The syntax for this method is as follows:

`jsonObject.put(String key, Object value);`

where `key` is the name of the element to be updated and `value` is the new value for the element.

**Section 3: Save the JSONObject**

Once the JSONObject is updated, it needs to be saved back to the JSON file. This can be done using the `write()` method. The syntax for this method is as follows:

`jsonObject.write(Writer writer);`

where `writer` is an instance of `java.io.Writer` that is used to write the JSONObject to the file.

**Section 4: Close the Writer**

Once the JSONObject is written to the file, the `Writer` needs to be closed to ensure that the changes are saved. This can be done using the `close()` method. The syntax for this method is as follows:

`writer.close();`
