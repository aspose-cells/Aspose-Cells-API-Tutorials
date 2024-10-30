---
title: Render Slicers in Aspose.Cells .NET
linktitle: Render Slicers in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/excel-slicers-management/render-slicers/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Slicers
{
    class RenderingSlicer
    {        
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Main()
        {
            // ExStart: 1
            // Load sample Excel file containing slicer.
            Workbook wb = new Workbook(sourceDir + "sampleRenderingSlicer.xlsx");

            // Access first worksheet.
            Worksheet ws = wb.Worksheets[0];

            // Set the print area because we want to render slicer only.
            ws.PageSetup.PrintArea = "B15:E25";

            // Specify image or print options, set one page per sheet and only area to true.
            Aspose.Cells.Rendering.ImageOrPrintOptions imgOpts = new Aspose.Cells.Rendering.ImageOrPrintOptions();
            imgOpts.HorizontalResolution = 200;
            imgOpts.VerticalResolution = 200;
            imgOpts.ImageType = Aspose.Cells.Drawing.ImageType.Png;
            imgOpts.OnePagePerSheet = true;
            imgOpts.OnlyArea = true;

            // Create sheet render object and render worksheet to image.
            Aspose.Cells.Rendering.SheetRender sr = new Aspose.Cells.Rendering.SheetRender(ws, imgOpts);
            sr.ToImage(0, outputDir + "outputRenderingSlicer.png");
            // ExEnd: 1

            Console.WriteLine("RenderingSlicer executed successfully.");
        }

    }
}

```
