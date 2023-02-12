---
title: What is the correct way to format a timestamp in a JSON response?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use a date/time library to convert the timestamp into an ISO-8601 formatted string before sending it in the JSON.
---

**Contents**

[TOC]

## Section 1: Setting Up the Timestamp

The first step in formatting a timestamp in JSON is to set up the timestamp in the desired format. This can be done by using a library like Moment.js to format the timestamp into the desired format.

## Section 2: Adding the Timestamp to the JSON

Once the timestamp has been set up, it can then be added to the JSON. This can be done by adding the timestamp as a value to a key in the JSON. For example, if the timestamp is to be added to an object with the key “timestamp”, the following code can be used:

```
{
   "timestamp": <timestamp>
}
```

Where <timestamp> is the formatted timestamp.

## Section 3: Outputting the JSON

Once the timestamp has been added to the JSON, it can then be outputted. This can be done by using the JSON.stringify() method. This will output the JSON with the timestamp included.

## Section 4: Testing the Output

Finally, it is important to test the outputted JSON to ensure that the timestamp is in the correct format. This can be done by using a JSON validator to check that the timestamp is in the correct format.
