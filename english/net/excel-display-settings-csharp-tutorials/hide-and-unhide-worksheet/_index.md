---
title: Hide And Unhide Worksheet
linktitle: Hide And Unhide Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 90
url: /net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
### Sample source code for Hide And Unhide Worksheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
            // Instantiating a Workbook object with opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);
            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];
            // Hiding the first worksheet of the Excel file
            worksheet.IsVisible = false;
            // Shows first worksheet of the Excel file
            //Worksheet.IsVisible = true;
            // Saving the modified Excel file in default (that is Excel 2003) format
            workbook.Save(dataDir + "output.out.xls");
            // Closing the file stream to free all resources
            fstream.Close();
```