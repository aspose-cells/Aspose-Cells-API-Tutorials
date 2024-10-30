---
title: Remove Slicers in Aspose.Cells .NET
linktitle: Remove Slicers in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/excel-slicers-management/remove-slicers/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Slicers
{
    class RemovingSlicer
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Main()
        {
            // Load sample Excel file containing slicer.
            Workbook wb = new Workbook(sourceDir + "sampleRemovingSlicer.xlsx");

            // Access first worksheet.
            Worksheet ws = wb.Worksheets[0];

            // Access the first slicer inside the slicer collection.
            Aspose.Cells.Slicers.Slicer slicer = ws.Slicers[0];

            // Remove slicer.
            ws.Slicers.Remove(slicer);

            // Save the workbook in output XLSX format.
            wb.Save(outputDir + "outputRemovingSlicer.xlsx", SaveFormat.Xlsx);

            Console.WriteLine("RemovingSlicer executed successfully.");
        }

    }
}

```
