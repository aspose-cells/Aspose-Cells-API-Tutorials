---
title: Freeze Panes Of Worksheet
linktitle: Freeze Panes Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 70
url: /net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
### Sample source code for Freeze Panes Of Worksheet using Aspose.Cells for .NET 
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
            // Applying freeze panes settings
            worksheet.FreezePanes(3, 2, 3, 2);
            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");
            // Closing the file stream to free all resources
            fstream.Close();
```