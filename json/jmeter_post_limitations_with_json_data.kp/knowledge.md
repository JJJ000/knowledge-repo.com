---
title: Jmeter is not capable of sending JSON data via a post request
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: No, JMeter does not send JSON data in POST requests.
---

**Contents**

[TOC]

Yes

#### Sending JSON

JMeter can send JSON data in the POST request. To send JSON data in POST request, use the Json Post Processor. This processor allows you to extract values from the JSON response and store them as JMeter variables.

#### Configuring JSON Post Processor

To configure the JSON Post Processor, you need to add it as a child element of the HTTP Request sampler. You can then configure the processor to extract the values from the response.

#### Using Variables

Once you have extracted the values from the JSON response, you can use them as variables in subsequent requests. This allows you to dynamically set values in your requests based on the response of the previous request.

#### Conclusion

In conclusion, JMeter can send JSON data in POST requests and extract values from the JSON response. This allows you to use the extracted values as variables in subsequent requests.
