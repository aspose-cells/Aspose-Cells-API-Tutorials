---
title: Add Arc Control with Connection Points
linktitle: Add Arc Control with Connection Points
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 27
url: /net/excel-shapes-controls/add-arc-control-with-connection-points/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Controls
{
    public class AddingArcControl
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

            // Add an arc shape.
            Aspose.Cells.Drawing.ArcShape arc1 = excelbook.Worksheets[0].Shapes.AddArc(2, 0, 2, 0, 130, 130);

            // Set the fill shape color
            arc1.Fill.FillType = FillType.Solid;
            arc1.Fill.SolidFill.Color = Color.Blue;

            // Set the placement of the arc.
            arc1.Placement = PlacementType.FreeFloating;           

            // Set the line weight.
            arc1.Line.Weight = 1;      

            // Set the dash style of the arc.
            arc1.Line.DashStyle = MsoLineDashStyle.Solid;

            // Add another arc shape.
            Aspose.Cells.Drawing.ArcShape arc2 = excelbook.Worksheets[0].Shapes.AddArc(9, 0, 2, 0, 130, 130);
            
            // Set the line color
            arc2.Line.FillType = FillType.Solid;
            arc2.Line.SolidFill.Color = Color.Blue;

            // Set the placement of the arc.
            arc2.Placement = PlacementType.FreeFloating;          

            // Set the line weight.
            arc2.Line.Weight = 1;           

            // Set the dash style of the arc.
            arc2.Line.DashStyle = MsoLineDashStyle.Solid;

            // Save the excel file.
            excelbook.Save(dataDir + "book1.out.xls");
            // ExEnd:1
        }
    }
}

```
