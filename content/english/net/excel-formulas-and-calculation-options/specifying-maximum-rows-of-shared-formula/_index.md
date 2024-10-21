---
title: Specifying Maximum Rows of Shared Formula in Excel
linktitle: Specifying Maximum Rows of Shared Formula in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 21
url: /net/excel-formulas-and-calculation-options/specifying-maximum-rows-of-shared-formula/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Formulas
{
    class SpecifyMaximumRowsOfSharedFormula
    {
        //Output directory
        static string outputDir = RunExamples.Get_OutputDirectory();

        public static void Run()
        {
            Workbook wb = new Workbook();

            //Set the max rows of shared formula to 5
            wb.Settings.MaxRowsOfSharedFormula = 5;

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Access cell D1
            Cell cell = ws.Cells["D1"];

            //Set the shared formula in 100 rows
            cell.SetSharedFormula("=Sum(A1:A2)", 100, 1);

            //Save the output Excel file
            wb.Save(outputDir + "outputSpecifyMaximumRowsOfSharedFormula.xlsx");

            Console.WriteLine("SpecifyMaximumRowsOfSharedFormula executed successfully.");
        }
    }
}

```
