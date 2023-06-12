---
title: Display And Hide Scroll Bars Of Worksheet
linktitle: Display And Hide Scroll Bars Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 50
url: /net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
### Sample source code for Display And Hide Scroll Bars Of Worksheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);
            // Hiding the vertical scroll bar of the Excel file
            workbook.Settings.IsVScrollBarVisible = false;
            // Hiding the horizontal scroll bar of the Excel file
            workbook.Settings.IsHScrollBarVisible = false;
            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");
            // Closing the file stream to free all resources
            fstream.Close();
```