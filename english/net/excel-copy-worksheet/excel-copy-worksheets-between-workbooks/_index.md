---
title: Excel Copy Worksheets Between Workbooks
linktitle: Excel Copy Worksheets Between Workbooks
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 30
url: /net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
### Sample source code for Excel Copy Worksheets Between Workbooks using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            string InputPath = dataDir + "book1.xls";
            // Create a Workbook.
            // Open a file into the first book.
            Workbook excelWorkbook0 = new Workbook(InputPath);
            // Create another Workbook.
            Workbook excelWorkbook1 = new Workbook();
            // Copy the first sheet of the first book into second book.
            excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
            // Save the file.
            excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```