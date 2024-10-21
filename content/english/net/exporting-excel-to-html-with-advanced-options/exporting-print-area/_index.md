---
title: Exporting Print Area to Html in Excel Programmatically
linktitle: Exporting Print Area to Html in Excel Programmatically
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/exporting-excel-to-html-with-advanced-options/exporting-print-area/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.HTML
{
    class ExportPrintAreaToHtml
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Main()
        {
            // ExStart:1
            // Load the Excel file.
            Workbook wb = new Workbook(sourceDir + "sampleInlineCharts.xlsx");

            // Access the sheet
            Worksheet ws = wb.Worksheets[0];

            // Set the print area.
            ws.PageSetup.PrintArea = "D2:M20";

            // Initialize HtmlSaveOptions
            HtmlSaveOptions options = new HtmlSaveOptions();

            // Set flag to export print area only
            options.ExportPrintAreaOnly = true;

            //Save to HTML format
            wb.Save(outputDir + "outputInlineCharts.html", options);
            // ExEnd:1
            Console.WriteLine("ExportPrintAreaToHtml executed successfully.");
        }
    }

}

```
