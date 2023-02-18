---
title: What is the best way to output JSON from an azure function?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Return a JSON object from the function`s output binding.
---

**Contents**

[TOC]

**Section 1: Create an Azure Function**

1. Log in to the [Azure Portal](https://portal.azure.com).
2. Click the **+ Create a resource** button in the top left corner.
3. Search for **Function App** in the search bar.
4. Click **Create**.
5. Enter a **Name** for the Function App.
6. Select a **Subscription**.
7. Select a **Resource Group** or create a new one.
8. Select a **Hosting Plan**.
9. Select a **Storage Account** or create a new one.
10. Click **Create**.

**Section 2: Create a Function**

1. Once the Function App is created, click on the Function App in the portal.
2. Click the **+** sign next to **Functions**.
3. Select **HTTP trigger**.
4. Enter a **Name** for the function.
5. Select a **Authorization level**.
6. Click **Create**.

**Section 3: Return JSON**

1. In the code editor, add the code to return the JSON.

```
using System.Net;

public static async Task<HttpResponseMessage> Run(HttpRequestMessage req, TraceWriter log)
{
    log.Info("C# HTTP trigger function processed a request.");

    var response = req.CreateResponse(HttpStatusCode.OK);
    response.Content = new StringContent("{\"message\":\"Hello World!\"}", Encoding.UTF8, "application/json");

    return response;
}
```

2. Click **Save**.

**Section 4: Test the Function**

1. Click the **Test** tab.
2. Enter a **Request body**.
3. Click **Run**.
4. View the **Response body** to see the JSON returned.
