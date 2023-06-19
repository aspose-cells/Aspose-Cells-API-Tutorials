---
title: Excel Move Worksheet
linktitle: Excel Move Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 40
url: /net/excel-copy-worksheet/excel-move-worksheet/
---
### Sample source code for Excel Move Worksheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            string InputPath = dataDir + "book1.xls";
            // Open an existing excel file.
            Workbook wb = new Workbook(InputPath);
            // Create a Worksheets object with reference to
            // the sheets of the Workbook.
            WorksheetCollection sheets = wb.Worksheets;
            // Get the first worksheet.
            Worksheet worksheet = sheets[0];
            // Move the first sheet to the third position in the workbook.
            worksheet.MoveTo(2);
            // Save the excel file.
            wb.Save(dataDir + "MoveWorksheet_out.xls");
```