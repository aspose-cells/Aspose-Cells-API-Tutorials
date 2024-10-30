---
title: Render Sequential Pages in Aspose.Cells
linktitle: Render Sequential Pages in Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 18
url: /net/rendering-and-export/render-limited-number-of-sequential-pages/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells.Rendering;

namespace Aspose.Cells.Examples.CSharp.Rendering
{
    class RenderLimitedNoOfSequentialPages 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Load the sample Excel file
            Workbook wb = new Workbook(sourceDir + "sampleImageOrPrintOptions_PageIndexPageCount.xlsx");

            //Access the first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Specify image or print options
            //We want to print pages 4, 5, 6, 7
            ImageOrPrintOptions opts = new ImageOrPrintOptions();
            opts.PageIndex = 3;
            opts.PageCount = 4;
            opts.ImageType = Drawing.ImageType.Png;

            //Create sheet render object
            SheetRender sr = new SheetRender(ws, opts);

            //Print all the pages as images
            for (int i = opts.PageIndex; i < sr.PageCount; i++)
            {
                sr.ToImage(i, outputDir + "outputImage-" + (i + 1) + ".png");
            }

            Console.WriteLine("RenderLimitedNoOfSequentialPages executed successfully.\r\n");
        }
    }
}

```
