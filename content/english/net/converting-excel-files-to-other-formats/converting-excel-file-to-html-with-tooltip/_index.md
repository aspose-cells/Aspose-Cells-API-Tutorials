---
title: Converting Excel File to HTML with Tooltip in .NET
linktitle: Converting Excel File to HTML with Tooltip in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/converting-excel-files-to-other-formats/converting-excel-file-to-html-with-tooltip/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging
{
    public class ConvertExcelFileToHtmlWithTooltip
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            // ExStart:1
            // Open the template file
            Workbook workbook = new Workbook(sourceDir + "AddTooltipToHtmlSample.xlsx");

            HtmlSaveOptions options = new HtmlSaveOptions();
            options.AddTooltipText = true;

            // Save as Markdown
            workbook.Save(outputDir + "AddTooltipToHtmlSample_out.html", options);
            // ExEnd:1

            Console.WriteLine("ConvertExcelFileToHtmlWithTooltip executed successfully.");
        }
    }
}

```
