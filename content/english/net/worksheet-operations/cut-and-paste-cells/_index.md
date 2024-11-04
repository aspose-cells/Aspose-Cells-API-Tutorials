---
title: Cut and Paste Cells within Worksheet
linktitle: Cut and Paste Cells within Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/worksheet-operations/cut-and-paste-cells/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets
{
    class CutAndPasteCells
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string outDir = "Your Document Directory";

            Workbook workbook = new Workbook();
            Worksheet worksheet = workbook.Worksheets[0];

            worksheet.Cells[0, 2].Value = 1;
            worksheet.Cells[1, 2].Value = 2;
            worksheet.Cells[2, 2].Value = 3;
            worksheet.Cells[2, 3].Value = 4;
            worksheet.Cells.CreateRange(0, 2, 3, 1).Name = "NamedRange";

            Range cut = worksheet.Cells.CreateRange("C:C");
            worksheet.Cells.InsertCutCells(cut, 0, 1, ShiftType.Right);
            workbook.Save(outDir + "CutAndPasteCells.xlsx");
            // ExEnd:1

            Console.WriteLine("CutAndPasteCells executed successfully.");
        }
    }
}

```
