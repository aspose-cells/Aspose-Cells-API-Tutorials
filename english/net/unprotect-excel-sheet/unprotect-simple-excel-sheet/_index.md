---
title: Unprotect Simple Excel Sheet
linktitle: Unprotect Simple Excel Sheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 30
url: /net/unprotect-excel-sheet/unprotect-simple-excel-sheet/
---
### Sample source code for Unprotect Simple Excel Sheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Instantiating a Workbook object
            Workbook workbook = new Workbook(dataDir + "book1.xls");
            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];
            // Unprotecting the worksheet without a password
            worksheet.Unprotect();
            // Saving the Workbook
            workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```