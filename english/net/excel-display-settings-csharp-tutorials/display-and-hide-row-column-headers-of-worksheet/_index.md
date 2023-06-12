---
title: Display And Hide Row Column Headers Of Worksheet
linktitle: Display And Hide Row Column Headers Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 40
url: /net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
### Sample source code for Display And Hide Row Column Headers Of Worksheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);
            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];
            // Hiding the headers of rows and columns
            worksheet.IsRowColumnHeadersVisible = false;
            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");
            // Closing the file stream to free all resources
            fstream.Close(); 
```