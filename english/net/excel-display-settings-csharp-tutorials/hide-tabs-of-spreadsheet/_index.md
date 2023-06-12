---
title: Hide Tabs Of Spreadsheet
linktitle: Hide Tabs Of Spreadsheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 100
url: /net/excel-display-settings-csharp-tutorials/hide-tabs-of-spreadsheet/
---
### Sample source code for Hide Tabs Of Spreadsheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Opening the Excel file
            Workbook workbook = new Workbook(dataDir + "book1.xls");
            // Hiding the tabs of the Excel file
            workbook.Settings.ShowTabs = false;
            // Shows the tabs of the Excel file
            //workbook.Settings.ShowTabs = true;
            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");
```