---
title: Excel Copy Worksheet
linktitle: Excel Copy Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 20
url: /net/excel-copy-worksheet/excel-copy-worksheet/
---
### Sample source code for Excel Copy Worksheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            string InputPath = dataDir + "book1.xls";
            // Open an existing Excel file.
            Workbook wb = new Workbook(InputPath);
            // Create a Worksheets object with reference to
            // the sheets of the Workbook.
            WorksheetCollection sheets = wb.Worksheets;
            // Copy data to a new sheet from an existing
            // sheet within the Workbook.
            sheets.AddCopy("Sheet1");
            // Save the Excel file.
            wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```