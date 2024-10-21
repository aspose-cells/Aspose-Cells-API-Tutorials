---
title: Setting Single Sheet Tab Name in HTML Export
linktitle: Setting Single Sheet Tab Name in HTML Export
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 21
url: /net/exporting-excel-to-html-with-advanced-options/setting-single-sheet-tab-name/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.HTML
{
    class SetSingleSheetTabNameInHtml
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Main()
        {
            // ExStart:1
            // Load the sample Excel file containing single sheet only
            Workbook wb = new Workbook(sourceDir + "sampleSingleSheet.xlsx");

            // Specify HTML save options
            Aspose.Cells.HtmlSaveOptions options = new Aspose.Cells.HtmlSaveOptions();

            // Set optional settings if required
            options.Encoding = System.Text.Encoding.UTF8;
            options.ExportImagesAsBase64 = true;
            options.ExportGridLines = true;
            options.ExportSimilarBorderStyle = true;
            options.ExportBogusRowData = true;
            options.ExcludeUnusedStyles = true;
            options.ExportHiddenWorksheet = true;

            //Save the workbook in Html format with specified Html Save Options
            wb.Save(outputDir + "outputSampleSingleSheet.htm", options);
            // ExEnd:1
            Console.WriteLine("SetSingleSheetTabNameInHtml executed successfully.");
        }
    }

}

```
