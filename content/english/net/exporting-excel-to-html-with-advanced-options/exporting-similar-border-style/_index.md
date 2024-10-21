---
title: Exporting Similar Border Style Programmatically in Excel
linktitle: Exporting Similar Border Style Programmatically in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/exporting-excel-to-html-with-advanced-options/exporting-similar-border-style/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.HTML
{
    class ExportSimilarBorderStyle
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Run()
        {
            //Load the sample Excel file
            Workbook wb = new Workbook(sourceDir + "sampleExportSimilarBorderStyle.xlsx");

            //Specify Html Save Options - Export Similar Border Style
            HtmlSaveOptions opts = new HtmlSaveOptions();
            opts.ExportSimilarBorderStyle = true;

            //Save the workbook in Html format with specified Html Save Options
            wb.Save(outputDir + "outputExportSimilarBorderStyle.html", opts);

            Console.WriteLine("ExportSimilarBorderStyle executed successfully.");
        }
    }

}

```
