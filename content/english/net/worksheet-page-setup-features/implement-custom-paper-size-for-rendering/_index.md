---
title: Implement Custom Paper Size in Worksheet for Rendering
linktitle: Implement Custom Paper Size in Worksheet for Rendering
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/worksheet-page-setup-features/implement-custom-paper-size-for-rendering/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class ImplementCustomPaperSizeOfWorksheetForRendering
    {
        public static void Run()
        {
            //Output directory
            string outputDir = "Your Document Directory";

            //Create workbook object
            Workbook wb = new Workbook();

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Set custom paper size in unit of inches
            ws.PageSetup.CustomPaperSize(6, 4);

            //Access cell B4
            Cell b4 = ws.Cells["B4"];

            //Add the message in cell B4
            b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");

            //Save the workbook in pdf format
            wb.Save(outputDir + "outputCustomPaperSize.pdf");

        }
    }
}

```
