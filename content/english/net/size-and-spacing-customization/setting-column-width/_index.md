---
title: Set Column Width in Pixels with Aspose.Cells for .NET
linktitle: Set Column Width in Pixels with Aspose.Cells for .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/size-and-spacing-customization/setting-column-width/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.HeightAndWidth
{
    public class SetColumnWidthInPixels
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
            worksheet.Cells.SetColumnWidthPixel(7, 200);

            workbook.Save(outDir + "SetColumnWidthInPixels_Out.xlsx");
            // ExEnd:1

            Console.WriteLine("SetColumnWidthInPixels executed successfully.");
        }
    }
}

```
