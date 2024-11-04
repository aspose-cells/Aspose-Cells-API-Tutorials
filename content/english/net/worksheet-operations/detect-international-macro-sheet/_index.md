---
title: Detect International Macro Sheet in Workbook
linktitle: Detect International Macro Sheet in Workbook
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/worksheet-operations/detect-international-macro-sheet/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Worksheets
{
    class DetectInternationalMacroSheet
    {
        public static void Run()
        {
            //ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

            //Load source Excel file
            Workbook workbook = new Workbook(sourceDir + "InternationalMacroSheet.xlsm");

            //Get Sheet Type
            SheetType sheetType = workbook.Worksheets[0].Type;

            //Print Sheet Type
            Console.WriteLine("Sheet Type: " + sheetType);
            //ExEnd:1

            Console.WriteLine("DetectInternationalMacroSheet executed successfully.");
        }
    }
}

```
