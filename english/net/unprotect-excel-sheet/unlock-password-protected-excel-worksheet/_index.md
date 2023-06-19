---
title: Unlock Password Protected Excel Worksheet
linktitle: Unlock Password Protected Excel Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 10
url: /net/unprotect-excel-sheet/unlock-password-protected-excel-worksheet/
---
### Sample source code for Unlock Password Protected Excel Worksheet using Aspose.Cells for .NET 
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
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```