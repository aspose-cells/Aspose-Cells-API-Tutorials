---
title: Set Column View Width in Pixels with Aspose.Cells for .NET
linktitle: Set Column View Width in Pixels with Aspose.Cells for .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/size-and-spacing-customization/setting-column-view-width/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.HeightAndWidth
{
    public class SetColumnViewWidthInPixels
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";
            string outDir = "Your Document Directory";

            //Load source Excel file
            Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");

            //Access first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Set the width of the column in pixels
            worksheet.Cells.SetViewColumnWidthPixel(7, 200);

            workbook.Save(outDir + "SetColumnViewWidthInPixels_Out.xlsx");
            // ExEnd:1

            Console.WriteLine("SetColumnViewWidthInPixels executed successfully.");
        }
    }
}

```
