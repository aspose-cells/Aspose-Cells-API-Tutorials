---
title: Add Validation Area to Cells in Excel
linktitle: Add Validation Area to Cells in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-data-validation-filter/add-validation-area-to-cells-in-excel/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class AddValidationArea
    {
        public static void Run()
        {
            // ExStart:1
            // directories
            string SourceDir = "Your Document Directory"();
            string outputDir = "Your Document Directory"();

            Workbook workbook = new Workbook(SourceDir + "ValidationsSample.xlsx");

            // Access first worksheet.
            Worksheet worksheet = workbook.Worksheets[0];

            // Accessing the Validations collection of the worksheet
            Validation validation = worksheet.Validations[0];

            // Create your cell area.
            CellArea cellArea = CellArea.CreateCellArea("D5", "E7");

            // Adding the cell area to Validation
            validation.AddArea(cellArea, false, false);

            // Save the output workbook.
            workbook.Save(outputDir + "ValidationsSample_out.xlsx");
            // ExEnd:1

            Console.WriteLine("AddValidationArea executed successfully.");
        }
    }
}
```
