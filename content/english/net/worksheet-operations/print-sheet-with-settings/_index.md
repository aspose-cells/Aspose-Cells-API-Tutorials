---
title: Print Sheet with Additional Settings
linktitle: Print Sheet with Additional Settings
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 19
url: /net/worksheet-operations/print-sheet-with-settings/
---

## Complete Source Code
```csharp
using Aspose.Cells.Rendering;
using System;
using System.Collections.Generic;
using System.Drawing.Printing;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Worksheets
{
    class PrintSheetWithAdditionalSettings
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

            //Load source Excel file
            Workbook workbook = new Workbook(sourceDir + "SheetRenderSample.xlsx");

            ImageOrPrintOptions imgOpt = new ImageOrPrintOptions();

            //Access first worksheet
            Worksheet worksheet = workbook.Worksheets[1];

            SheetRender sheetRender = new SheetRender(worksheet, imgOpt);

            PrinterSettings printerSettings = new PrinterSettings();
            printerSettings.PrinterName = "<PRINTER NAME>";
            printerSettings.Copies = 2;

            sheetRender.ToPrinter(printerSettings);
            // ExEnd:1
        }
    }
}

```
