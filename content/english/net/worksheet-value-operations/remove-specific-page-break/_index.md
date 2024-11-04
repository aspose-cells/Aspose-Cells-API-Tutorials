---
title: Remove Specific Page Break from Worksheet using Aspose.Cells
linktitle: Remove Specific Page Break from Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/worksheet-value-operations/remove-specific-page-break/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Value
{
    public class RemoveSpecificPageBreak
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook(dataDir + "PageBreaks.xls");

            // Removing a specific page break
            workbook.Worksheets[0].HorizontalPageBreaks.RemoveAt(0);
            workbook.Worksheets[0].VerticalPageBreaks.RemoveAt(0);

            // Save the Excel file.
            workbook.Save(dataDir + "RemoveSpecificPageBreak_out.xls");
            // ExEnd:1
        }
    }
}

```
