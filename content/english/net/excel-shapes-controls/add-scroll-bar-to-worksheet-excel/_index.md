---
title: Add Scroll Bar to Worksheet in Excel
linktitle: Add Scroll Bar to Worksheet in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 22
url: /net/excel-shapes-controls/add-scroll-bar-to-worksheet-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Controls
{
    public class AddingScrollBarControl
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

            // Get the first worksheet.
            Worksheet worksheet = excelbook.Worksheets[0];

            // Invisible the gridlines of the worksheet.
            worksheet.IsGridlinesVisible = false;

            // Get the worksheet cells.
            Cells cells = worksheet.Cells;

            // Input a value into A1 cell.
            cells["A1"].PutValue(1);

            // Set the font color of the cell.
            cells["A1"].GetStyle().Font.Color = Color.Maroon;

            // Set the font text bold.
            cells["A1"].GetStyle().Font.IsBold = true;

            // Set the number format.
            cells["A1"].GetStyle().Number = 1;

            // Add a scrollbar control.
            Aspose.Cells.Drawing.ScrollBar scrollbar = worksheet.Shapes.AddScrollBar(0, 0, 1, 0, 125, 20);

            // Set the placement type of the scrollbar.
            scrollbar.Placement = PlacementType.FreeFloating;

            // Set the linked cell for the control.
            scrollbar.LinkedCell = "A1";

            // Set the maximum value.
            scrollbar.Max = 20;

            // Set the minimum value.
            scrollbar.Min = 1;

            // Set the incr. change for the control.
            scrollbar.IncrementalChange = 1;

            // Set the page change attribute.
            scrollbar.PageChange = 5;

            // Set it 3-D shading.
            scrollbar.Shadow = true;

            // Save the excel file.
            excelbook.Save(dataDir + "book1.out.xls");
            // ExEnd:1

        }
    }
}

```
