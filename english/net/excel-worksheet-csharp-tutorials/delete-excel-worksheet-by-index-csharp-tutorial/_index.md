---
title: Delete Excel Worksheet By Index C# Tutorial
linktitle: Delete Excel Worksheet By Index C# Tutorial
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 30
url: /net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-index-csharp-tutorial/
---
### Sample source code for Delete Excel Worksheet By Index C# Tutorial using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);
            // Removing a worksheet using its sheet index
            workbook.Worksheets.RemoveAt(0);
            // Save workbook
            workbook.Save(dataDir + "output.out.xls");
```