---
title: Exporting Comments while Saving Excel File to HTML
linktitle: Exporting Comments while Saving Excel File to HTML
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/saving-and-exporting-excel-files-with-options/exporting-comments/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging 
{
    public class ExportCommentsWhileSavingExcelFileToHtml 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Load sample Excel file
            Workbook wb = new Workbook(sourceDir + "sampleExportCommentsHTML.xlsx");

            //Export comments - set IsExportComments property to true
            HtmlSaveOptions opts = new HtmlSaveOptions();
            opts.IsExportComments = true;

            //Save the Excel file to HTML
            wb.Save(outputDir + "outputExportCommentsHTML.html", opts);
           
            Console.WriteLine("ExportCommentsWhileSavingExcelFileToHtml executed successfully.\r\n");
        }
    }
}

```
