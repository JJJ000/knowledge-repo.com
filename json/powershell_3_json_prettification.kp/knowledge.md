---
title: Format JSON in powershell 3
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: The ConvertFrom-Json cmdlet can be used to prettify JSON in PowerShell 3.
---

**Contents**

[TOC]

## Using ConvertTo-Json

The `ConvertTo-Json` cmdlet can be used to prettify JSON in PowerShell 3. It is part of the `Microsoft.PowerShell.Utility` module, which is included with Windows PowerShell.

To prettify a JSON string, simply pipe it to `ConvertTo-Json`:

```powershell
$jsonString | ConvertTo-Json
```

## Using Format-Table

Another option for prettifying JSON in PowerShell 3 is to use the `Format-Table` cmdlet. This cmdlet is part of the `Microsoft.PowerShell.Utility` module, which is included with Windows PowerShell.

To prettify a JSON string, simply pipe it to `Format-Table`:

```powershell
$jsonString | Format-Table
```

## Using Out-String

The `Out-String` cmdlet can also be used to prettify JSON in PowerShell 3. It is part of the `Microsoft.PowerShell.Utility` module, which is included with Windows PowerShell.

To prettify a JSON string, simply pipe it to `Out-String`:

```powershell
$jsonString | Out-String
```

## Using Format-List

The `Format-List` cmdlet can also be used to prettify JSON in PowerShell 3. It is part of the `Microsoft.PowerShell.Utility` module, which is included with Windows PowerShell.

To prettify a JSON string, simply pipe it to `Format-List`:

```powershell
$jsonString | Format-List
```
