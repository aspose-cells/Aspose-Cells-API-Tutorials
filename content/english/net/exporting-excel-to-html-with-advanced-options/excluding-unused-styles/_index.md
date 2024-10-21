---
title: Excluding Unused Styles while Exporting Excel to HTML
linktitle: Excluding Unused Styles while Exporting Excel to HTML
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/exporting-excel-to-html-with-advanced-options/excluding-unused-styles/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.HTML
{
    class ExcludeUnusedStylesInExcelToHTML
    {
        public static void Run()
        {
            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();

            //Create workbook
            Workbook wb = new Workbook();

            //Create an unused named style
            wb.CreateStyle().Name = "UnusedStyle_XXXXXXXXXXXXXX";

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Put some value in cell C7
            ws.Cells["C7"].PutValue("This is sample text.");

            //Specify html save options, we want to exclude unused styles
            HtmlSaveOptions opts = new HtmlSaveOptions();

            //Comment this line to include unused styles
            opts.ExcludeUnusedStyles = true;

            //Save the workbook in html format
            wb.Save(outputDir + "outputExcludeUnusedStylesInExcelToHTML.html", opts);

            Console.WriteLine("ExcludeUnusedStylesInExcelToHTML executed successfully.");
        }
    }
}

```
