---
title: Export Slicer to PDF using Aspose.Cells .NET
linktitle: Export Slicer to PDF using Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/excel-slicers-management/export-slicer-to-pdf/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Slicers
{
    class ExportSlicerToPDF
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Run()
        {
            // ExStart:1
            Workbook workbook = new Workbook(sourceDir + "SampleSlicerChart.xlsx");
            workbook.Save(outputDir + "SampleSlicerChart.pdf", SaveFormat.Pdf);
            // ExEnd:1

            Console.WriteLine("ExportSlicerToPDF executed successfully.");
        }

    }
}

```
