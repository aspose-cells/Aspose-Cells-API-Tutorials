---
title: Format Slicers in Aspose.Cells .NET
linktitle: Format Slicers in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/excel-slicers-management/format-slicers/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Slicers
{
    class FormattingSlicer
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Main()
        {
            // Load sample Excel file containing slicer.
            Workbook wb = new Workbook(sourceDir + "sampleFormattingSlicer.xlsx");

            // Access first worksheet.
            Worksheet ws = wb.Worksheets[0];

            // Access the first slicer inside the slicer collection.
            Aspose.Cells.Slicers.Slicer slicer = ws.Slicers[0];

            // Set the number of columns of the slicer.
            slicer.NumberOfColumns = 2;

            // Set the type of slicer style.
            slicer.StyleType = Aspose.Cells.Slicers.SlicerStyleType.SlicerStyleLight6;

            // Save the workbook in output XLSX format.
            wb.Save(outputDir + "outputFormattingSlicer.xlsx", SaveFormat.Xlsx);

            Console.WriteLine("FormattingSlicer executed successfully.");
        }
    }
}

```
