---
title: What changes do I need to make in Chrome to get ASP.NET web API to return json instead of xml?
authors:
- cool_wizard
tags:
- c#
- asp.net
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-18 00:00:00
updated_at: 2023-01-18 00:00:00
tldr: Set the `Accept` header to `application/json` in the request.
---

**Contents**

[TOC]

### Enable Chrome to Accept JSON

1. Open Chrome and type in `chrome://flags` in the address bar.
2. Search for `Web Platform Features` and enable the `Experimental Web Platform features` flag.

### Configure ASP.NET Web API to Return JSON

1. Open the `WebApiConfig.cs` file.
2. Add the following line of code to the `Register` method:

```c#
config.Formatters.JsonFormatter.SupportedMediaTypes.Add(new MediaTypeHeaderValue("text/html"));
```

### Test the Configuration

1. Run the application and make an HTTP request.
2. Check the response headers to verify that the response is in JSON format.

### Troubleshooting

1. If the response is still in XML format, check the `WebApiConfig.cs` file to make sure the `SupportedMediaTypes` line of code is present.
2. If the response is still in XML format, check the Chrome `Experimental Web Platform features` flag to make sure it is enabled.
