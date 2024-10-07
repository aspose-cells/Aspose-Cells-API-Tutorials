---
title: Create Union Range of Cells in Excel
linktitle: Create Union Range of Cells in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-range-address-calculation/create-union-range-of-cells-in-excel/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class CreateUnionRange
    {
        public static void Run()
        {
            // ExStart:1
            // Output directory
            string outputDir = "Your Document Directory"();

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Create union range
            UnionRange unionRange = workbook.Worksheets.CreateUnionRange("sheet1!A1:A10,sheet1!C1:C10", 0);

            // Put value "ABCD" in the range
            unionRange.Value = "ABCD";

            // Save the output workbook.
            workbook.Save(outputDir + "CreateUnionRange_out.xlsx");
            // ExEnd:1

            Console.WriteLine("CreateUnionRange executed successfully.");
        }
    }
}
```
