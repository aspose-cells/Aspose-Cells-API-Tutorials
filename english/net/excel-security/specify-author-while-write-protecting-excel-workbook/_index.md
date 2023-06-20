---
title: Specify Author While Write Protecting Excel Workbook
linktitle: Specify Author While Write Protecting Excel Workbook
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 30
url: /net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

### Sample source code for Specify Author While Write Protecting Excel Workbook using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = "YOUR SOURCE DIRECTORY";

//Output directory
string outputDir = "YOUR OUTPUT DIRECTORY";

// Create empty workbook.
Workbook wb = new Workbook();

// Write protect workbook with password.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Specify author while write protecting workbook.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Save the workbook in XLSX format.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```
