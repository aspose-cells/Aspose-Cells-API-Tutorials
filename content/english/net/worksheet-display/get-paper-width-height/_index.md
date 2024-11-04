---
title: Get Paper Width and Height for Worksheet Printing
linktitle: Get Paper Width and Height for Worksheet Printing
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/worksheet-display/get-paper-width-height/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Display
{
    public class GetPaperWidthHeight
    {
        public static void Run()
        {
            //Create workbook
            Workbook wb = new Workbook();

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Set paper size to A2 and print paper width and height in inches
            ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
            Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

            //Set paper size to A3 and print paper width and height in inches
            ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
            Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

            //Set paper size to A4 and print paper width and height in inches
            ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
            Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

            //Set paper size to Letter and print paper width and height in inches
            ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
            Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

        }
    }
}

```
