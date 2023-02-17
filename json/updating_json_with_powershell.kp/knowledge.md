---
title: What is the process for updating a JSON file using powershell?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: You can use the ConvertFrom-Json and ConvertTo-Json cmdlets to update a JSON file using PowerShell.
---

**Contents**

[TOC]

## Section 1: Retrieve JSON File

The first step to updating a JSON file using PowerShell is to retrieve the JSON file. This can be done by using the `Invoke-WebRequest` cmdlet. The `Invoke-WebRequest` cmdlet allows you to retrieve the contents of a web page or file. To retrieve the JSON file, use the following command:

```powershell
Invoke-WebRequest -Uri <URL of JSON file> -OutFile <local file path>
```

## Section 2: Load JSON File

Once the JSON file has been retrieved, it needs to be loaded into a PowerShell object. This can be done using the `ConvertFrom-Json` cmdlet. The `ConvertFrom-Json` cmdlet allows you to convert a JSON string or file into a PowerShell object. To load the JSON file, use the following command:

```powershell
$jsonObject = Get-Content <local file path> | ConvertFrom-Json
```

## Section 3: Modify JSON Object

Once the JSON file has been loaded into a PowerShell object, it can be modified using the `Set-Variable` cmdlet. The `Set-Variable` cmdlet allows you to set the value of a variable. To modify the JSON object, use the following command:

```powershell
Set-Variable -Name <JSON object property> -Value <new value>
```

## Section 4: Export JSON File

Once the JSON object has been modified, it can be exported back to a JSON file using the `ConvertTo-Json` cmdlet. The `ConvertTo-Json` cmdlet allows you to convert a PowerShell object into a JSON string or file. To export the JSON file, use the following command:

```powershell
$jsonObject | ConvertTo-Json -Depth 10 | Out-File <local file path>
```
