---
title: Implement Print Area of Worksheet
linktitle: Implement Print Area of Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 25
url: /net/worksheet-page-setup-features/implement-print-area/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class SetPrintArea
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Obtaining the reference of the PageSetup of the worksheet
            PageSetup pageSetup = workbook.Worksheets[0].PageSetup;

            // Specifying the cells range (from A1 cell to T35 cell) of the print area
            pageSetup.PrintArea = "A1:T35";

            // Save the workbook.
            workbook.Save(dataDir + "SetPrintArea_out.xls");
            // ExEnd:1
        }
    }
}

```
