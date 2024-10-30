---
title: Output Blank Page if Nothing to Print in Aspose.Cells
linktitle: Output Blank Page if Nothing to Print in Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 17
url: /net/rendering-and-export/output-blank-page-when-nothing-to-print/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells.Rendering;
using System.Drawing.Imaging;

namespace Aspose.Cells.Examples.CSharp.Rendering 
{
    public class OutputBlankPageWhenThereIsNothingToPrint 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Create workbook
            Workbook wb = new Workbook();

            //Access first worksheet - it is empty sheet
            Worksheet ws = wb.Worksheets[0];

            //Specify image or print options
            //Since the sheet is blank, we will set OutputBlankPageWhenNothingToPrint to true
            //So that empty page gets printed
            ImageOrPrintOptions opts = new ImageOrPrintOptions();
            opts.ImageType = Drawing.ImageType.Png;
            opts.OutputBlankPageWhenNothingToPrint = true;

            //Render empty sheet to png image
            SheetRender sr = new SheetRender(ws, opts);
            sr.ToImage(0, outputDir + "OutputBlankPageWhenNothingToPrint.png");

            Console.WriteLine("OutputBlankPageWhenThereIsNothingToPrint executed successfully.\r\n");
        }
    }
}

```
