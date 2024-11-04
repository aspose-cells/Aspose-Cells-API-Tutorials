---
title: Add Page Breaks in Worksheet using Aspose.Cells
linktitle: Add Page Breaks in Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/worksheet-value-operations/add-page-breaks/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Value
{
    public class AddingPageBreaks
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Add a page break at cell Y30
            workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
            workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");

            // Save the Excel file.
            workbook.Save(dataDir + "AddingPageBreaks_out.xls");
            // ExEnd:1
        }
    }
}

```
