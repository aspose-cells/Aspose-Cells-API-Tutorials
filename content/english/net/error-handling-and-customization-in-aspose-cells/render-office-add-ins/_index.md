---
title: Render Office Add-ins in Excel to PDF with Aspose.Cells
linktitle: Render Office Add-ins in Excel to PDF with Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/error-handling-and-customization-in-aspose-cells/render-office-add-ins/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Rendering
{
    class RenderOfficeAdd_InsWhileConvertingExcelToPdf 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Load the sample Excel file containing Office Add-Ins
            Workbook wb = new Workbook(sourceDir + "sampleRenderOfficeAdd-Ins.xlsx");

            //Save it to Pdf format
            wb.Save(outputDir + "output-" + CellsHelper.GetVersion() + ".pdf");

            Console.WriteLine("RenderOfficeAdd_InsWhileConvertingExcelToPdf executed successfully.");
        }
    }
}

```
