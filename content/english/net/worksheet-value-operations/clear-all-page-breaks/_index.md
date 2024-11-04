---
title: Clear All Page Breaks from Worksheet using Aspose.Cells
linktitle: Clear All Page Breaks from Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/worksheet-value-operations/clear-all-page-breaks/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Value
{
    public class ClearAllPageBreaks
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Clearing all page breaks
            workbook.Worksheets[0].HorizontalPageBreaks.Clear();
            workbook.Worksheets[0].VerticalPageBreaks.Clear();

            // Save the Excel file.
            workbook.Save(dataDir + "ClearAllPageBreaks_out.xls");
            // ExEnd:1
        }
    }
}

```
