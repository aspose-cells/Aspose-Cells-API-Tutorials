---
title: Add Excel Worksheet To Existing Workbook C# Tutorial
linktitle: Add Excel Worksheet To Existing Workbook C# Tutorial
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 10
url: /net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
### Sample source code for Add Excel Worksheet To Existing Workbook C# Tutorial using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);
            // Adding a new worksheet to the Workbook object
            int i = workbook.Worksheets.Add();
            // Obtaining the reference of the newly added worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[i];
            // Setting the name of the newly added worksheet
            worksheet.Name = "My Worksheet";
            // Saving the Excel file
            workbook.Save(dataDir + "output.out.xls");
            // Closing the file stream to free all resources
            fstream.Close();
```