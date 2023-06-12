---
title: Remove Panes Of Worksheet
linktitle: Remove Panes Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 120
url: /net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
### Sample source code for Remove Panes Of Worksheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Instantiate a new workbook and Open a template file
            Workbook book = new Workbook(dataDir + "Book1.xls");
            // Set the active cell
            book.Worksheets[0].ActiveCell = "A20";
            // Split the worksheet window
            book.Worksheets[0].RemoveSplit();
            // Save the excel file
            book.Save(dataDir + "output.xls");
```