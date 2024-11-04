---
title: Print Preview of Workbook using Aspose.Cells
linktitle: Print Preview of Workbook using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 23
url: /net/workbook-operations/print-preview/
---

## Complete Source Code
```csharp
using Aspose.Cells.Rendering;
using Aspose.Cells.WebExtensions;
using System;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    public class PrintPreview
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

            Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
            ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
            WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
            Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);

            SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
            Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
            // ExEnd:1

            Console.WriteLine("PrintPreview executed successfully.");
        }
    }
}

```
