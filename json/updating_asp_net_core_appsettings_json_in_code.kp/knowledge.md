---
title: Updating the appsettings.json file in an ASP.NET core application using code
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: The appsettings.json file can be updated in code using the ConfigurationBuilder class.
---

**Contents**

[TOC]

# Section 1: Updating the appsettings.json from the Code

Appsettings.json can be updated from the code by using the ConfigurationBuilder class. This is provided by the Microsoft.Extensions.Configuration namespace. The ConfigurationBuilder class allows us to read and write configuration data from various sources such as appsettings.json, environment variables, command line arguments, and more.

# Section 2: Steps to Update the appsettings.json

1. Create an instance of the ConfigurationBuilder class.
2. Add the appsettings.json file as the configuration source.
3. Use the SetBasePath() method to specify the path to the file.
4. Use the AddJsonFile() method to read the appsettings.json file.
5. Use the GetSection() method to get the specific section of the file.
6. Use the SetValue() method to update the value of the particular section.
7. Use the Save() method to save the changes to the file.

# Section 3: Example Code

The following code snippet shows how to update the appsettings.json from the code.

```
// Create an instance of the ConfigurationBuilder class
var builder = new ConfigurationBuilder();

// Add the appsettings.json file as the configuration source
builder.AddJsonFile("appsettings.json");

// Use the SetBasePath() method to specify the path to the file
builder.SetBasePath(Path.Combine(Directory.GetCurrentDirectory(), "config"));

// Use the GetSection() method to get the specific section of the file
var section = builder.GetSection("AppSettings");

// Use the SetValue() method to update the value of the particular section
section["Key1"] = "Value1";

// Use the Save() method to save the changes to the file
builder.Save();
```

# Section 4: Summary

In summary, appsettings.json can be updated from the code using the ConfigurationBuilder class. This class allows us to read and write configuration data from various sources such as appsettings.json, environment variables, command line arguments, and more. To update the appsettings.json from the code, we need to create an instance of the ConfigurationBuilder class, add the appsettings.json file as the configuration source, use the SetBasePath() method to specify the path to the file, use the AddJsonFile() method to read the appsettings.json file, use the GetSection() method to get the specific section of the file, use the SetValue() method to update the value of the particular section, and use the Save() method to save the changes to the file.
