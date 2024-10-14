---
title: Add Oval to Worksheet in Excel
linktitle: Add Oval to Worksheet in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 17
url: /net/excel-shapes-controls/add-oval-to-worksheet-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Controls
{
    public class AddingOvalControl
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

            // Add an oval shape.
            Aspose.Cells.Drawing.Oval oval1 = excelbook.Worksheets[0].Shapes.AddOval(2, 0, 2, 0, 130, 160);

            // Set the placement of the oval.
            oval1.Placement = PlacementType.FreeFloating; 
         
            // Set the line weight.
            oval1.Line.Weight = 1;

            // Set the dash style of the oval.
            oval1.Line.DashStyle = MsoLineDashStyle.Solid;

            // Add another oval (circle) shape.
            Aspose.Cells.Drawing.Oval oval2 = excelbook.Worksheets[0].Shapes.AddOval(9, 0, 2, 15, 130, 130);

            // Set the placement of the oval.
            oval2.Placement = PlacementType.FreeFloating;

            // Set the line weight.
            oval2.Line.Weight = 1;     

            // Set the dash style of the oval.
            oval2.Line.DashStyle = MsoLineDashStyle.Solid;

            // Save the excel file.
            excelbook.Save(dataDir + "book1.out.xls");
            // ExEnd:1

        }
    }
}

```
