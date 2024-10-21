---
title: Hiding Overlaid Content with Cross Hide Right while Saving to Html
linktitle: Hiding Overlaid Content with Cross Hide Right while Saving to Html
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/exporting-excel-to-html-with-advanced-options/hiding-overlaid-content-with-cross-hide-right/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.HTML
{
    class HidingOverlaidContentWithCrossHideRightWhileSavingToHtml
    { 
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Main()
        {
            //Load sample Excel file 
            Workbook wb = new Workbook(sourceDir + "sampleHidingOverlaidContentWithCrossHideRightWhileSavingToHtml.xlsx");

            //Specify HtmlSaveOptions - Hide Overlaid Content with CrossHideRight while saving to Html
            HtmlSaveOptions opts = new HtmlSaveOptions();
            opts.HtmlCrossStringType = HtmlCrossType.CrossHideRight;

            //Save to HTML with HtmlSaveOptions
            wb.Save(outputDir + "outputHidingOverlaidContentWithCrossHideRightWhileSavingToHtml.html", opts);

            Console.WriteLine("HidingOverlaidContentWithCrossHideRightWhileSavingToHtml executed successfully.");
        }
    }
}

```
