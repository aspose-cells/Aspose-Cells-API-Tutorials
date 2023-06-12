---
title: Display Tab Of Spreadsheet
linktitle: Display Tab Of Spreadsheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 60
url: /net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
### Sample source code for Display Tab Of Spreadsheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Instantiating a Workbook object
            // Opening the Excel file
            Workbook workbook = new Workbook(dataDir + "book1.xls");
            // Hiding the tabs of the Excel file
            workbook.Settings.ShowTabs = true;
            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");
```