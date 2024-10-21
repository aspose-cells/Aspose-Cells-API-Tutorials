---
title: Disabling Downlevel Revealed Comments while Saving to HTML
linktitle: Disabling Downlevel Revealed Comments while Saving to HTML
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/loading-and-saving-excel-files-with-options/disabling-downlevel-revealed-comments/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging 
{
    public class DisableDownlevelRevealedCommentsWhileSavingToHTML 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Load sample workbook
            Workbook wb = new Workbook(sourceDir + "sampleDisableDownlevelRevealedComments.xlsx");

            //Disable DisableDownlevelRevealedComments
            HtmlSaveOptions opts = new HtmlSaveOptions();
            opts.DisableDownlevelRevealedComments = true;

            //Save the workbook in html
            wb.Save(outputDir + "outputDisableDownlevelRevealedComments_true.html", opts);
            
            Console.WriteLine("DisableDownlevelRevealedCommentsWhileSavingToHTML executed successfully.\r\n");
        }
    }
}

```
