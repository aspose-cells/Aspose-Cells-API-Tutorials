---
title: Create Summary Row Below with Aspose.Cells for .NET
linktitle: Create Summary Row Below with Aspose.Cells for .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/row-and-column-management/summary-row-below/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.Grouping
{
    public class SummaryRowBelow
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Workbook workbook = new Workbook(dataDir + "sample.xlsx");
            Worksheet worksheet = workbook.Worksheets[0];

            // Grouping first six rows and first three columns
            worksheet.Cells.GroupRows(0, 5, true);
            worksheet.Cells.GroupColumns(0, 2, true);

            // Setting SummaryRowBelow property to false
            worksheet.Outline.SummaryRowBelow = false;

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");
            // ExEnd:1
        }
    }
}

```
