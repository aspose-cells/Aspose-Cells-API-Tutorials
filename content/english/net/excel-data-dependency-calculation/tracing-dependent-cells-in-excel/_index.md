---
title: Tracing Dependent Cells in Excel
linktitle: Tracing Dependent Cells in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-data-dependency-calculation/tracing-dependent-cells-in-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Data.Processing
{
    public class TracingDependents
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);
            
            Workbook workbook = new Workbook(dataDir + "Book1.xlsx");
            Cells cells = workbook.Worksheets[0].Cells;
            Cell cell = cells["B2"];

           Cell[] ret = cell.GetDependents(true);

            foreach (Cell c in cell.GetDependents(true))
            {
                Console.WriteLine(c.Name);
            }
            // ExEnd:1
            Console.ReadKey();
        }
    }
}

```
