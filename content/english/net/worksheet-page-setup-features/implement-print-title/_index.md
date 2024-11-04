---
title: Implement Print Title in Worksheet
linktitle: Implement Print Title in Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 27
url: /net/worksheet-page-setup-features/implement-print-title/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class SetPrintTitle
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Obtaining the reference of the PageSetup of the worksheet
            Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;

            // Defining column numbers A & B as title columns
            pageSetup.PrintTitleColumns = "$A:$B";

            // Defining row numbers 1 & 2 as title rows
            pageSetup.PrintTitleRows = "$1:$2";

            // Save the workbook.
            workbook.Save(dataDir + "SetPrintTitle_out.xls");
            // ExEnd:1
        }
    }
}

```
