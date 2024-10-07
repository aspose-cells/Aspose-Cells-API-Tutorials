---
title: Change Excel Cells Alignment Without Losing Formatting
linktitle: Change Excel Cells Alignment Without Losing Formatting
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-data-alignment-formatting/change-cells-alignment-in-excel-without-losing-existing-formatting/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Data
{
    class ChangeCellsAlignmentAndKeepExistingFormatting
    {
        //Source directory
        static string sourceDir = "Your Document Directory"();

        //Output directory
        static string outputDir = "Your Document Directory"();

        public static void Main()
        {
            // Load sample Excel file containing cells with formatting.
            Workbook wb = new Workbook(sourceDir + "sampleChangeCellsAlignmentAndKeepExistingFormatting.xlsx");

            // Access first worksheet.
            Worksheet ws = wb.Worksheets[0];

            // Create cells range.
            Range rng = ws.Cells.CreateRange("B2:D7");

            // Create style object.
            Style st = wb.CreateStyle();

            // Set the horizontal and vertical alignment to center.
            st.HorizontalAlignment = TextAlignmentType.Center;
            st.VerticalAlignment = TextAlignmentType.Center;

            // Create style flag object.
            StyleFlag flag = new StyleFlag();

            // Set style flag alignments true. It is most crucial statement.
            // Because if it will be false, no changes will take place.
            flag.Alignments = true;

            // Apply style to range of cells.
            rng.ApplyStyle(st, flag);

            // Save the workbook in XLSX format.
            wb.Save(outputDir + "outputChangeCellsAlignmentAndKeepExistingFormatting.xlsx", SaveFormat.Xlsx);

            Console.WriteLine("ChangeCellsAlignmentAndKeepExistingFormatting executed successfully.");
        }
    }
}

```
