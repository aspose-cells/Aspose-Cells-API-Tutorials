---
title: Tracing Precedents in Excel
linktitle: Tracing Precedents in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-subtotal-calculation/tracing-precedents-in-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Data.Processing
{
    public class TracingPrecedents
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            
            Workbook workbook = new Workbook(dataDir + "Book1.xlsx");
            Cells cells = workbook.Worksheets[0].Cells;
            Cell cell = cells["B4"];

            ReferredAreaCollection ret = cell.GetPrecedents();
            ReferredArea area = ret[0];
            Console.WriteLine(area.SheetName);
            Console.WriteLine(CellsHelper.CellIndexToName(area.StartRow, area.StartColumn));
            Console.WriteLine(CellsHelper.CellIndexToName(area.EndRow, area.EndColumn));
            // ExEnd:1
            Console.ReadKey();
        }
    }
}

```
