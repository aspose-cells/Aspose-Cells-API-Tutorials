---
title: Add Worksheets to Designer Spreadsheet using Aspose.Cells
linktitle: Add Worksheets to Designer Spreadsheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/worksheet-management/add-worksheets-to-designer-spreadsheet/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Management
{
    public class AddingWorksheetsToDesignerSpreadSheet
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            string InputPath = dataDir + "book1.xlsx";

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(InputPath, FileMode.Open);

           
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);


            // Adding a new worksheet to the Workbook object
            int i = workbook.Worksheets.Add();

            // Obtaining the reference of the newly added worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[i];

            // Setting the name of the newly added worksheet
            worksheet.Name = "My Worksheet";

            // Saving the Excel file
            workbook.Save(dataDir + "output.xlsx");
            // ExEnd:1
        }
    }
}

```
