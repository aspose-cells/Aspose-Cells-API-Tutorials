---
title: Get Paper Width And Height Of Worksheet
linktitle: Get Paper Width And Height Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 80
url: /net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
### Sample source code for Get Paper Width And Height Of Worksheet using Aspose.Cells for .NET 
```csharp
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
```