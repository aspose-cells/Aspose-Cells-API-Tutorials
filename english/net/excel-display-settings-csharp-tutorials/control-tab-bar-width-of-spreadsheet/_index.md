---
title: Control Tab Bar Width Of Spreadsheet
linktitle: Control Tab Bar Width Of Spreadsheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 10
url: /net/excel-display-settings-csharp-tutorials/control-tab-bar-width-of-spreadsheet/
---
### Sample source code for Control Tab Bar Width Of Spreadsheet using Aspose.Cells for .NET 
```csharp
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Instantiating a Workbook object
            // Opening the Excel file
            Workbook workbook = new Workbook(dataDir + "book1.xls");
            // Hiding the tabs of the Excel file
            workbook.Settings.ShowTabs = true;
            // Adjusting the sheet tab bar width
            workbook.Settings.SheetTabBarWidth = 800;
            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");
```