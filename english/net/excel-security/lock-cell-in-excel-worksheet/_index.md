---
title: Lock Cell In Excel Worksheet
linktitle: Lock Cell In Excel Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 20
url: /net/excel-security/lock-cell-in-excel-worksheet/
---
### Sample source code for Lock Cell In Excel Worksheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            Workbook workbook = new Workbook(dataDir + "Book1.xlsx");
            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];
            worksheet.Cells["A1"].GetStyle().IsLocked = true;
            // Finally, Protect the sheet now.
            worksheet.Protect(ProtectionType.All);
            workbook.Save(dataDir + "output.xlsx");
```