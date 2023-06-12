---
title: Get Excel Worksheet By Name C# Tutorial
linktitle: Get Excel Worksheet By Name C# Tutorial
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 50
url: /net/excel-worksheet-csharp-tutorials/get-excel-worksheet-by-name-csharp-tutorial/
---
### Sample source code for Get Excel Worksheet By Name C# Tutorial using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            string InputPath = dataDir + "book1.xlsx";
            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(InputPath, FileMode.Open);
            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);
            // Accessing a worksheet using its sheet name
            Worksheet worksheet = workbook.Worksheets["Sheet1"];
            Cell cell = worksheet.Cells["A1"];
            Console.WriteLine(cell.Value);
```