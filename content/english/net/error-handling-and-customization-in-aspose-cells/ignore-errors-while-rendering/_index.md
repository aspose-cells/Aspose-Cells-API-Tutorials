---
title: Ignore Errors in Excel to PDF Rendering with Aspose.Cells
linktitle: Ignore Errors in Excel to PDF Rendering with Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/error-handling-and-customization-in-aspose-cells/ignore-errors-while-rendering/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Rendering
{
    class IgnoreErrorsWhileRenderingExcelToPdf 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Load the Sample Workbook that throws Error on Excel2Pdf conversion
            Workbook wb = new Workbook(sourceDir + "sampleErrorExcel2Pdf.xlsx");

            //Specify Pdf Save Options - Ignore Error
            PdfSaveOptions opts = new PdfSaveOptions();
            opts.IgnoreError = true;

            //Save the Workbook in Pdf with Pdf Save Options
            wb.Save(outputDir + "outputErrorExcel2Pdf.pdf", opts);

            Console.WriteLine("IgnoreErrorsWhileRenderingExcelToPdf executed successfully.\r\n");
        }
    }
}

```
