---
title: Add Check Box to Worksheet in Excel
linktitle: Add Check Box to Worksheet in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 18
url: /net/excel-shapes-controls/add-checkbox-to-worksheet-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Controls
{
    public class AddingCheckBoxControl
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Create directory if it is not already present.
            bool IsExists = System.IO.Directory.Exists(dataDir);
            if (!IsExists)
                System.IO.Directory.CreateDirectory(dataDir);

            // Instantiate a new Workbook.
            Workbook excelbook = new Workbook();

            // Add a checkbox to the first worksheet in the workbook.
            int index = excelbook.Worksheets[0].CheckBoxes.Add(5, 5, 100, 120);

            // Get the checkbox object.
            Aspose.Cells.Drawing.CheckBox checkbox = excelbook.Worksheets[0].CheckBoxes[index];

            // Set its text string.
            checkbox.Text = "Click it!";

            // Put a value into B1 cell.
            excelbook.Worksheets[0].Cells["B1"].PutValue("LnkCell");

            // Set B1 cell as a linked cell for the checkbox.
            checkbox.LinkedCell = "B1";

            // Check the checkbox by default.
            checkbox.Value = true;

            // Save the excel file.
            excelbook.Save(dataDir + "book1.out.xls");
            // ExEnd:1

        }
    }
}

```
