---
title: Read Glow Effect of Shape in Excel
linktitle: Read Glow Effect of Shape in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/excel-shape-text-modifications/read-glow-effect-shape-excel/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.OLE
{
    public class ReadColorGlowEffect
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //Read the source excel file
            Workbook wb = new Workbook(dataDir + "sourceGlowEffectColor.xlsx");

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Access the shape
            Shape sh = ws.Shapes[0];

            //Read the glow effect color and its various properties
            GlowEffect ge = sh.Glow;
            CellsColor clr = ge.Color;
            Console.WriteLine("Color: " + clr.Color);
            Console.WriteLine("ColorIndex: " + clr.ColorIndex);
            Console.WriteLine("IsShapeColor: " + clr.IsShapeColor);
            Console.WriteLine("Transparency: " + clr.Transparency);
            Console.WriteLine("Type: " + clr.Type);

        }
    }
}

```
