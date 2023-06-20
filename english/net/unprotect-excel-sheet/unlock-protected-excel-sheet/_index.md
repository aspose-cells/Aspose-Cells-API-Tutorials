---
title: Unlock Protected Excel Sheet
linktitle: Unlock Protected Excel Sheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 20
url: /net/unprotect-excel-sheet/unlock-protected-excel-sheet/
---
### Sample source code for Unlock Protected Excel Sheet using Aspose.Cells for .NET 
```csharp
try
{
    // The path to the documents directory.
    string dataDir = "YOUR DOCUMENT DIRECTORY";
    // Instantiating a Workbook object
    Workbook workbook = new Workbook(dataDir + "book1.xls");
    // Accessing the first worksheet in the Excel file
    Worksheet worksheet = workbook.Worksheets[0];
    // Unprotecting the worksheet with a password
    worksheet.Unprotect("");
    // Save Workbook
    workbook.Save(dataDir + "output.out.xls");
}
catch(Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```