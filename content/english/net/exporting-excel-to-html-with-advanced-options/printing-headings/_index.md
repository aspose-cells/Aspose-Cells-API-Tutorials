---
title: Printing Headings Programmatically in Excel
linktitle: Printing Headings Programmatically in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 18
url: /net/exporting-excel-to-html-with-advanced-options/printing-headings/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.HTML
{
    class PrintHeadings
    {
        public static void Run()
        {
            // ExStart:1
            // Input directory
            string sourceDir = "Your Document Directory";

            // Output directory
            string outputDir = "Your Document Directory";
            // ExStart:1

            //Load sample source file
            Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");

            HtmlSaveOptions options = new HtmlSaveOptions();
            options.ExportHeadings = true;

            // Save the workbook
            workbook.Save(outputDir + "PrintHeadings_out.html", options);
            // ExEnd:1

            Console.WriteLine("PrintHeadings executed successfully.\r\n");
        }
    }
}

```
