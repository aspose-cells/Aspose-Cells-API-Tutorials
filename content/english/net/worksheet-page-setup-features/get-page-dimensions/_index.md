---
title: Get Page Dimensions of Worksheet
linktitle: Get Page Dimensions of Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/worksheet-page-setup-features/get-page-dimensions/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    class GetPageDimensions
    {
        public static void Run()
        {
            
            // Create an instance of Workbook class
            Workbook book = new Workbook();

            // Access first worksheet
            Worksheet sheet = book.Worksheets[0];

            // Set paper size to A2 and print paper width and height in inches
            sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
            Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);

            // Set paper size to A3 and print paper width and height in inches
            sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
            Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);

            // Set paper size to A4 and print paper width and height in inches
            sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
            Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);

            // Set paper size to Letter and print paper width and height in inches
            sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
            Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);

            Console.WriteLine("GetPageDimensions executed successfully.\r\n");

        }
    }
}

```
